<!-- TopBar.vue -->
<template>
    <div class="top-bar" :class="{ 'is-scrolled-down': isScrolledDown }">
      <div class="top-bar-content">
        <div>
          <a href="https://maps.app.goo.gl/aLX5KuAphy4vmi5M8">
            <span>Adresse : Rue du Baron d'Obin 132 - 4219 Wasseiges</span>
          </a>
          <span style="margin-left: 10px;">
            Lundi - dimanche: 17h30 - 21h | Mercredi 11h30 - 13h30
          </span>
        </div>
        <div>
          <span>0489 18 45 70</span>
        </div>
      </div>
    </div>
  </template>

<script>
export default {
  props: {
    isScrolledDown: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
  /* Your existing styles for the top bar */

  .top-bar {
    height: 30px;
    background-color: #f0f0f0;
    border-bottom: 1px solid #ccc;
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 1000;
    transition: transform 0.3s ease-in-out;
  }

  .top-bar-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    color: #333;
  }

  .is-scrolled-down .top-bar {
    transform: translateY(-100%);
  }
</style>
