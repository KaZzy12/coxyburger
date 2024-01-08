<template>
    <div class="section" id="burgers">
      <h2>Burgers</h2>
      <div class="burger-container">
        <!-- Loop through the burgers array and display them -->
        <div v-for="burger in listBurgers" :key="burger.id" class="burger-item">
          <!-- Burger content goes here -->
          <div class="burger-content">
            <img :src="burger.image" alt="Burger Image">
            <div class="burger-details">
              <h3>{{ burger.name }}</h3>
              <p>{{ burger.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>

<script>
import { burgers } from '../burgers/burgers';

const listBurgers = burgers;

export default {
  data() {
    return {
      listBurgers,
    };
  },
};
</script>

<style scoped>
/* BurgersSection-specific styles */
.burger-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.burger-item {
  width: calc(33.33% - 10px);
  margin-bottom: 20px;
  text-align: center;
}

.burger-content {
  display: flex;
  align-items: flex-start; /* Align items to the top */
  flex-direction: row; /* Horizontal arrangement by default */
}

.burger-item img {
  width: 50%; /* Adjust the width as needed */
  height: auto; /* Maintain aspect ratio */
}

.burger-details {
  margin-top: 10px;
  text-align: center; /* Center text within the container */
}

@media screen and (max-width: 768px) {
  .burger-item {
    width: calc(50% - 10px);
  }

  .burger-content {
    flex-direction: column; /* Vertical arrangement on smaller screens */
  }
}

@media screen and (max-width: 480px) {
  .burger-item {
    width: 100%;
  }
}
</style>
