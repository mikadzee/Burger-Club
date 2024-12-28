<template>
  <div>
    <Header />
  </div>
  <main>
    <div class="container text-font" >
      <div class="block-1" id="home">
        <div class="title logo-font">
          <h2>THE ULTIMATE</h2>
          <h1>Burger Club</h1>
          <p>Savor the Flavor, Join the Club!</p>
  
          <div class="images-burgers">
            <img src="./assets/images/Frame 5.png" alt="">
            <img src="./assets/images/Frame 6.png" alt="">
            <img src="./assets/images/Frame 7.png" alt="">
            <img src="./assets/images/Frame 8.png" alt="">
          </div>
        </div>

        <div class="image">
          <img src="./assets/images/snapedit_1735060738455.png" alt="">
        </div>
      </div>

      <div 
        class="animated-div block-2"
        id="menu"
        :style="{ 'left': `${Math.min(Math.max(100 - blocks[0].progress, 0), 100)}%` }"
      >
        <h2 class="title-menu">Menu</h2>

        <div class="products">
          <div class="product" v-for="product in menu">
            <img :src="product.image" alt="">
            <h2>{{ product.title }}</h2>
          </div>
        </div>
      </div>


      <div 
        class="animated-div block-3" 
        :style="{ 'left': `${Math.min(Math.max(100 - blocks[1].progress, 0), 100)}%` }"
      >
        <h2 class="title-about">About</h2>

        <div class="text">
          <p><span>Burger Club</span> did not go down in history as the inventor of burgers, but we are making new history, here and now, by creating and successfully developing an international network of craft burger joints. We know how to create a masterpiece from simple ingredients that will make you come back to us again and again. We sell more than 2.7 million burgers a year, and the total weight of French fries sold per year is equal to the weight of three Boeings and 14 cars.<br><span>The company</span> began its journey back in 2008 with modest capabilities and enormous faith in its business. Thanks to this, the project has become one of the most successful in the CIS, three times included in the Forbes ranking of the most profitable franchises. During this time, more than 170 establishments were sold in 10 countries.<br><span>Burger CLUB</span> is a new generation of craft burger establishments, the menu of which is significantly smaller and more specialized - almost 50% of the offerings are burgers. All burgers in the chain's establishments are prepared according to original recipes developed by our technologists specifically for the Burger CLUB chain.</p>
        </div>
      </div>
    </div>

    <div style="height: 270vh;"></div>
  </main>
</template>

<style lang="less">
@import "./assets/styles/main.less";




.container {
  height: 100vh;
  background-color: #12372A;
  width: 100%;
  overflow: hidden;
  position: fixed;
  top: 0;

  & .block-1 {
    margin-left: 50px;
    display: flex;
    justify-content: center;
    @media(max-width: 600px) {
      margin-left: 0px;
    }
    & .title {
      margin-top: 200px;
      text-align: center;
      width: 50%;
  
      & > h2 {
        font-size: 40px;
        color: #ADBC9F;
      }
  
      & > h1 {
        font-size: 70px;
        margin-block-start: -10px;
      }
  
      & > p {
        font-size: 15px;
        color: #ADBC9F;
      }
      @media(max-width: 600px) {
        margin-top: 120px;
        width: 100%;
        & > h2 {
          font-size: 30px;
          color: #ADBC9F;
        }
    
        & > h1 {
          font-size: 60px;
        }
    
        & > p {
          font-size: 20px;
          color: #ADBC9F;
        }
      } 
      & .images-burgers {
        margin-top: 120px;
        display: flex;
        gap: 20px;
        justify-content: center;

        @media(max-width: 600px) {
          gap: 10px;
          flex-wrap: wrap;
          margin-top: 10px;

        }
      }
    }

    & .image {
      & > img {
        width: 90%;
        
        @media(max-width: 600px) {
          display: none;
        }
      }
    }
  }

  & .block-2 {
    padding: 0px 190px;

    @media (max-width: 600px) {
      padding: 0px 0px;
      
    }
    & .title-menu {
      margin-top: 60px;
      text-align: center;
      font-size: 40px;
      color: #FBFADA;

      @media (max-width: 600px) {
        margin-top: 80px;
        font-size: 30px;
      
      }
    }

    & .products {
      margin-top: 20px;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      gap: 15px;
      row-gap: 10px;
      @media (max-width: 600px) {
        margin-top: 10px;
      }
      & .product {
        padding: 20px 0px;
        position: relative;
        cursor: pointer;
        width: 250px;
        height: 280px;
        background: linear-gradient(#131313, #110000, #0000005d);
        border-radius: 15px;
        & > img {
          height: 190px;
        }
        
        & > h2 {
          margin: 0 auto;
          width: 150px;
          text-align: center;
          font-size: 20px;
        }
        @media (max-width: 600px) {
          margin-top: 10px;
          width: 150px;
          height: 220px;
          & > img {
            height: 150px;
          }

          & > h2 {
            margin: 0 auto;
            width: 100px;
            text-align: center;
            font-size: 15px;
          }
        }
      }
    }
  }

  & .block-3 {

    & .title-about {
      margin-top: 60px;
      text-align: center;
      font-size: 40px;
      color: #FBFADA;
      
      @media (max-width: 600px) {
        margin-top: 80px;
        font-size: 30px;
      }
    }

    & .text {
      margin-top: 20px;
      padding: 0px 150px;
      font-size: 20px;

      & > p {
        line-height: 34px;

        & > span {
          margin-left: 10px;
          font-weight: 700;
          color: red;
        }
      }
      @media (max-width: 600px) {
        margin-top: 20px;
        padding: 0px 30px;
        font-size: 18px;

        & > p {
          line-height: 34px;

          & > span {
            margin-left: 5px;
            font-weight: 700;
            color: red;
          }
        }
      }
    }
  }

  & .animated-div {
    position: absolute;
    transition: left 0.8s ease;
    top: 0px;
    left: 100%;
    height: 100vh;
    background-color: #12372A;
    width: 100%;
    overflow: auto;

    & h2 {
      color: #fff;
      text-align: center;
    }
    
  }
}

::-webkit-scrollbar {
  display: none;
}



</style>

<script setup>
import { ref, onMounted, watch } from 'vue';
import BURGER from "./assets/images/menu/BURGER.png";
import DESERTS from "./assets/images/menu/DESERTS AND BEVERAGES.png";
import FRIES from "./assets/images/menu/FRIES.png";
import LAUNCH from "./assets/images/menu/LAUNCH OFFER.png";
import Club from "./assets/images/menu/New In the Club.png";
import SALADS from "./assets/images/menu/SALADS.png";
import SIDES from "./assets/images/menu/SIDES.png";
import WRAPS from "./assets/images/menu/WRAPS.png";


const menu = ref([
  {title: "New In the Club", image: Club},
  {title: "BURGER", image: BURGER},
  {title: "SIDES", image: SIDES},
  {title: "FRIES", image: FRIES},
  {title: "DESERTS AND BEVERAGES", image: DESERTS},
  {title: "LAUNCH OFFER @99", image: LAUNCH},
  {title: "WRAPS", image: WRAPS},
  {title: "SALADS", image: SALADS},

])
const scrollY = ref(0);
const blocks = ref([
  { startScroll: 100, progress: 0 },
  { startScroll: 500, progress: 0 },
]);


function updateScrollY() {
  scrollY.value = window.scrollY;
}

onMounted(() => {
  window.scrollTo(0, 0)
  window.addEventListener('scroll', updateScrollY);
});


watch(scrollY, (newScrollY) => {
  blocks.value.forEach(block => {
    if (newScrollY >= block.startScroll) {

      block.progress = Math.min((newScrollY - block.startScroll) * 0.5, 100);
    } else {

      block.progress = 0;
    }
  });
});
</script>
