<template>
  <div id="app">
    <HeaderComponente></HeaderComponente>
      <!-- <LastArticle></LastArticle> -->
      <router-view></router-view>  
    <Footer></Footer>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import MiComponente from './components/MiComponente.vue';
import HeaderComponente from './components/HeaderComponente.vue';

// import LastArticle from './components/LastArticles.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    // HelloWorld,
    // MiComponente,
    HeaderComponente,
    // Slider,
    // Sidebar,
    // LastArticle,
    Footer
  }
}
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */

@import './assets/css/style.css';
</style>
