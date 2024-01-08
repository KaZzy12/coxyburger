<!-- TopBar.vue -->
<template>
    <div class="top-bar">
      <div class="top-bar-content">
        <div class="top-bar-item">
          <a href="https://maps.app.goo.gl/aLX5KuAphy4vmi5M8">
            <img class="icon" src="../assets/map_pin_icon.png">
            Rue du Baron d'Obin 132 - 4219 Wasseiges
          </a>
          <span style="margin-left: 10px;">
            <img class="icon" src="../assets/clock.png">
            Lundi - dimanche: 17h30 - 21h | Mercredi 11h30 - 13h30
          </span>
        </div>
        <div class = "top-bar-item">
          <img class="icon" src="../assets/phone.png">
          0489 18 45 70
        </div>
      </div>
    </div>
  </template>

<style scoped>
  .top-bar {
    height: 30px;
    background-color: #f0f0f0;
    border-bottom: 1px solid #ccc;
  }

  .top-bar-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 20px;
    color: #333;
  }
  .icon {
    bottom: 5px;
    height: 20px;
  }
.top-bar-item {
  text-decoration: none;
}
</style>
