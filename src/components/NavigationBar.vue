<template>
    <nav class="navbar">
      <div class="navbar-brand">
        <router-link
         :to="{name: 'Home'}"
         class="navbar-item">
         <img class="logo" src="../assets/coxyburger.png">
         Coxyburger
        </router-link>
      </div>
      <div class="navbar-menu">
        <ul class="menu-list">
          <li>
            <router-link class="navbar-item" :to="{name: 'Burgers'}" exact>
              Burgers
            </router-link>
          </li>
          <li>
            <router-link class="navbar-item" :to="{name: 'Carte'}" exact>
              Carte
            </router-link>
          </li>
          <li>
            <router-link class="navbar-item" :to="{name: 'Contact'}" exact>
              Contact
            </router-link>
          </li>
        </ul>
      </div>
    </nav>
</template>

<script>
export default {
  methods: {
    scrollToSection(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
  },
};
</script>
<style scoped>
.navbar {
  width: 97.5%;
  background: linear-gradient(180deg, #234b90 80%, #ffffff 81%, #922028 15%);
  padding: 0.7rem 1rem;
  display: flex;
  justify-content: space-between;
  align-items: center; /* Vertically center the content */
  border-radius: 10px; /* Add rounded corners */
}
.navbar-brand {
  color: white;
  font-size: 1.5rem;
}
.logo {
  vertical-align: middle;
  height: 80px;
}
.menu-list {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex; /* Display the menu items in a row */
}
.menu-list li {
  display: inline-block;
  margin-right: 1rem;
}
.navbar-item {
  color: white;
  text-decoration: none;
}
.sticky {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000; /* Adjust the z-index as needed */
  /* Add any additional styling for the sticky state */
}
</style>
