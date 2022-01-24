<template>
  <div id="nav">
    <Navbar/>
  </div>
  <router-view />
  <Footer />
</template>


<script>
import Footer from './components/Footer.vue';
import Navbar from './components/Navbar.vue';



export default {
  components: { Footer, Navbar }
  
}
</script>

<style>
@import "./assets/styles/style.css";
@import "./assets/styles/global.css";
@import "./assets/styles/colors.css";
</style>
