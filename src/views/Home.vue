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
      <img class="header-img03" src="" alt="">
      <img class="header-img04" src="" alt="">
      <img class="header-img05" src="" alt="">
      
    </div>

    <section class="product">
        <h2 class="product-category">Best selling</h2>

               <button class="pre-btn"><img src="../assets/img/arrow.png" alt=""></button>
                <button class="nxt-btn"><img src="../assets/img/arrow.png" alt=""></button>

              <div class="product-container">
                  <div class="product-card">
                    <div class="product-image">
                            <img src="../assets/img/macbookpro.jpg" class="product-thumb" alt="" >
                            <button class="card-btn">add to wishlist </button>
                    </div>
                        <h2 class="product-info"> brand</h2>
                        <p class="product-short-description"> a short line about the product</p>
                        <span class="price">$20</span>
                        <span class="actual-price">$40</span>
                  </div>

                   <div class="product-card">
                    <div class="product-image">
                            <img src="../assets/img/macbookpro.jpg" class="product-thumb" alt="" >
                            <button class="card-btn">add to wishlist </button>
                    </div>
                        <h2 class="product-info"> brand</h2>
                        <p class="product-short-description"> a short line about the product</p>
                        <span class="price">$20</span>
                        <span class="actual-price">$40</span>
                  </div>

                   <div class="product-card">
                    <div class="product-image">
                            <img src="../assets/img/macbookpro.jpg" class="product-thumb" alt="" >
                            <button class="card-btn">add to wishlist </button>
                    </div>
                        <h2 class="product-info"> brand</h2>
                        <p class="product-short-description"> a short line about the product</p>
                        <span class="price">$20</span>
                        <span class="actual-price">$40</span>
                  </div>

                   <div class="product-card">
                    <div class="product-image">
                            <img src="../assets/img/macbookpro.jpg" class="product-thumb" alt="" >
                            <button class="card-btn">add to wishlist </button>
                    </div>
                        <h2 class="product-info"> brand</h2>
                        <p class="product-short-description"> a short line about the product</p>
                        <span class="price">$20</span>
                        <span class="actual-price">$40</span>
                  </div>

                   <div class="product-card">
                    <div class="product-image">
                            <img src="../assets/img/macbookpro.jpg" class="product-thumb" alt="" >
                            <button class="card-btn">add to wishlist </button>
                    </div>
                        <h2 class="product-info"> brand</h2>
                        <p class="product-short-description"> a short line about the product</p>
                        <span class="price">$20</span>
                        <span class="actual-price">$40</span>
                  </div>

                   <div class="product-card">
                    <div class="product-image">
                            <img src="../assets/img/macbookpro.jpg" class="product-thumb" alt="" >
                            <button class="card-btn">add to wishlist </button>
                    </div>
                        <h2 class="product-info"> brand</h2>
                        <p class="product-short-description"> a short line about the product</p>
                        <span class="price">$20</span>
                        <span class="actual-price">$40</span>
                  </div>
              </div>

    </section>
    
    <v-col>
   
    </v-col>
    
  
</template>

<script>
const productContainers = [...document.querySelectorAll('.product-container')];
const nxtBtn = [...document.querySelectorAll('.nxt-btn')];
const preBtn = [...document.querySelectorAll('.pre-btn')];

productContainers.forEach((item, i) => {
    let containerDimensions = item.getBoundingClientRect();
    let containerWidth = containerDimensions.width;

    nxtBtn[i].addEventListener('click', () => {
        item.scrollLeft += containerWidth;
    })

    preBtn[i].addEventListener('click', () => {
        item.scrollLeft -= containerWidth;
    })
})






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
text-align: center;
}

.container img{
   height: 500px;
  width: 100% ;
  min-width: 100% ;
  max-width: 100% ;
  background-size: cover;
  background-position: center;


}

.header-img02{
    background-image: url("../assets/img/hero_watch.jpg");
   
}

.header-img03{
    background-image: url("../assets/img/macbookpro.jpg");
   
}

.header-img04{
    background-image: url("../assets/img/macbook_air_space.jpeg");
   
}

.header-img05{
    background-image: url("../assets/img/promo_watch_heart.jpg");
   

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


/* PRODUCTS SLIDER */
  .product {
  position: relative;
  overflow: hidden;
  padding: 20px;
}

.product-category {
  padding: 0 10vw;
  font-size: 30px;
  font-weight: 500;
  margin-bottom: 40px;
  text-transform: capitalize;
}

.product-container {
  padding: 0 10vw;
  display: flex;
  overflow-x: auto;
  scroll-behavior: smooth;
}

.product-container::-webkit-scrollbar {
  display: none;
}

.product-card {
  flex: 0 0 auto;
  width: 250px;
  height: 450px;
  margin-right: 40px;
}

.product-image {
  position: relative;
  width: 100%;
  height: 350px;
  overflow: hidden;
}

.product-thumb {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.discount-tag {
  position: absolute;
  background: #fff;
  padding: 5px;
  border-radius: 5px;
  color: silver;
  right: 10px;
  top: 10px;
  text-transform: capitalize;
}

.card-btn {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
  padding: 10px;
  width: 90%;
  text-transform: capitalize;
  border: none;
  outline: none;
  background: #fff;
  border-radius: 5px;
  transition: 0.5s;
  cursor: pointer;
  opacity: 0;
}

.product-card:hover .card-btn {
  opacity: 1;
}

.card-btn:hover {
  background: silver;
  color: #fff;
}

.product-info {
  width: 100%;
  height: 100px;
  padding-top: 10px;
}

.product-brand {
  text-transform: uppercase;
}

.product-short-description {
  width: 100%;
  height: 20px;
  line-height: 20px;
  overflow: hidden;
  opacity: 0.5;
  text-transform: capitalize;
  margin: 5px 0;
}

.price {
  font-weight: 900;
  font-size: 20px;
}

.actual-price {
  margin-left: 20px;
  opacity: 0.5;
  text-decoration: line-through;
}

.pre-btn,
.nxt-btn {
  border: none;
  width: 10vw;
  height: 100%;
  position: absolute;
  top: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(90deg, rgba(255, 255, 255, 0) 0%, #fff 100%);
  cursor: pointer;
  z-index: 8;
}

.pre-btn {
  left: 0;
  transform: rotate(180deg);
}

.nxt-btn {
  right: 0;
}

.pre-btn img,
.nxt-btn img {
  opacity: 0.2;
}

.pre-btn:hover img,
.nxt-btn:hover img {
  opacity: 1;
}

.collection-container {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 10px;
}

.collection {
  position: relative;
}

.collection img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.collection p {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: #fff;
  font-size: 50px;
  text-transform: capitalize;
}

.collection:nth-child(3) {
  grid-column: span 2;
  margin-bottom: 10px;
}


</style>
