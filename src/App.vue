<template>
  <div class ="header">
    <TopBar/>
    <NavigationBar/>
  </div>
  <div class="container">
    <main>
      <router-view/>
    </main>
  </div>
</template>

<script>
import TopBar from './components/TopBar.vue';
import NavigationBar from './components/NavigationBar.vue';

export default {
  name: 'App',
  components: {
    TopBar,
    NavigationBar,
  },
};
</script>

<style>
#app {
  font-family: Poppins;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
.header {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1000;
  transition: transform 0.3s ease-in-out;
}
.section {
  min-height: 100vh; /* Set each section to at least the height of the viewport */
  border: 1px solid #ddd;
  margin-bottom: 20px;
}
.content {
  padding-top: 100px; /* Adjust the padding to be at least the height of your navbar */
}
.container {
  margin-top: 150px;
}
</style>
