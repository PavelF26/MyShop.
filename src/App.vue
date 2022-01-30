<template>
  <div id="nav">
    <Navbar/>
  <router-view />
  <ScrollTopArrow/>
  
  <Footer />
  </div>
</template>


<script>
import Footer from './components/Footer.vue';
import Navbar from './components/Navbar.vue';
import ScrollTopArrow from './components/ScrollTopArrow.vue';




export default {
  components: { Footer, Navbar,ScrollTopArrow }
  
}
</script>

<style>
@import "./assets/styles/style.css";
@import "./assets/styles/global.css";
@import "./assets/styles/colors.css";

.btn-up {
    border-radius: 8px;
    background-color: rgba(0, 0, 0, 0.55);
    padding-top: 27px;
    padding-left: 10px;
    padding-right: 10px;
    padding-bottom: 5px;
}


</style>

