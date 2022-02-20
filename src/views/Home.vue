<template>
  <div>
    <div class="header-img">
      <div class="basic-slider ptb-200">
      <p class="jkl">iPhone 13pro</p>
        <div class="container">
          <div class="hero-caption pt-30">
            <div class="slider-content hero-text">
              
              <a class="btn">Shop Appl</a>
            </div>
          </div>
        </div>
      </div>
    </div>

    </div>
    <div class="container">
      
      <img class="header-img02" src="" alt="">
      <img class="header-img02" src="" alt="">
      <img class="header-img02" src="" alt="">
      <img class="header-img02" src="" alt="">
      
    </div>
    
    <v-col>
   
    </v-col>
    
  
</template>

<script>
export default {
  data: () => ({})
};
</script>

<style scoped>

.container {
  grid-template-columns: 1fr  1fr ;
  column-gap: 10px;
  row-gap: 15px;
  display: grid;
}

.header-img {
  background-image: url("../assets/img/hero_iphone_13pro.jpeg");
  height: 1020px;
  width: 450%;
  min-width: 100% !important;
  max-width: 100% !important;
  background-size: cover;
  background-position: center;
}

.jkl{
  font-size: 5em;
  color: black;
text-align: center;}

.header-img02{
    background-image: url("../assets/img/hero_watch.jpg");
    height: 500px;
  width: 100% ;
  min-width: 100% ;
  max-width: 100% ;
  background-size: cover;
  background-position: center;

}


.hero-caption {
  display: table;
  height: 100%;
  margin: 0 auto;
  position: relative;
  width: 80%;
  z-index: 2;
}
.hero-text {
  display: table-cell;
  height: 100%;
  position: relative;
  vertical-align: middle;
}
.basic-slider {
  position: relative;
}
.slider-content h2 {
  font-size: 42px;
  font-weight: 700;
  letter-spacing: 2px;
  margin: 0;
  margin-bottom: 20px;
}
</style>
