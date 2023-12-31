<template>
  <TopBar/>
  <NavigationBar/>
  <HelloWorld msg="Welcome to Your Vue.js App" class="content"/>
  <Burgers/>
  <Carte/>
  <Contact/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import TopBar from './components/TopBar.vue';
import NavigationBar from './components/NavigationBar.vue';
import Burgers from './components/Burgers.vue';
import Carte from './components/Carte.vue';
import Contact from './components/Contact.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    TopBar,
    NavigationBar,
    Burgers,
    Carte,
    Contact,
  },
  data() {
    return {
      isScrolledDown: false,
      prevScrollX: 0,
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    scrollToSection(sectionId) {
      this.$router.push({ name: sectionId });
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
    handleScroll() {
      const currentScrollX = window.scrollX;
      const currentScrollY = window.scrollY;

      // Check if scrolling vertically or horizontally
      if (currentScrollX !== this.prevScrollX) {
        // Scrolling horizontally, hide the top bar
        this.isScrolledDown = false;
      } else {
        // Scrolling vertically
        this.isScrolledDown = currentScrollY > 0;
      }

      // Update the previous scroll position
      this.prevScrollX = currentScrollX;
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
