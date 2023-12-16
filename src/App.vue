<template>
  <NavigationBar/>
  <HelloWorld msg="Welcome to Your Vue.js App" class="content"/>
  <Burgers/>
  <Carte/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import NavigationBar from './components/NavigationBar.vue';
import Burgers from './components/Burgers.vue';
import Carte from './components/Carte.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    NavigationBar,
    Burgers,
    Carte,
  },
  methods: {
    scrollToSection(sectionId) {
      this.$router.push({ name: sectionId });
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
.section {
  min-height: 100vh; /* Set each section to at least the height of the viewport */
  border: 1px solid #ddd;
  margin-bottom: 20px;
}
.content {
  padding-top: 100px; /* Adjust the padding to be at least the height of your navbar */
}
</style>
