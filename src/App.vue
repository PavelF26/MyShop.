<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view />
  <Footer />
</template>


<script>
import Footer from './components/Footer.vue';



export default {
  components: { Footer }
  
}
</script>

<style>
@import "./assets/styles/style.css";
@import "./assets/styles/global.css";
@import "./assets/styles/colors.css";
</style>
