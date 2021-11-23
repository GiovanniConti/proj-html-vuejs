<template>
  <header class="m-4">
    <div class="navbar p-0">
      <img :src="require('@/assets/img/' + logoHeader)" alt="Logo Header" class="img-nav">

      <ul class="navMenu list-inline m-0 fs-6 fw-bold">
        <li
          class="list-inline-item mx-4 p-1"
          v-for="(item, i) in navbarItems"
          :key="i"
        >{{ item }}</li>
        <li class="list-inline-item ms-4">
          <img src="@/assets/svg/svg-1.svg" alt="svg-navbar">
          </li>
      </ul>
    </div>
    <div class="hero container-xl my-4">
      <div class="row">
        <div class="col hero-text text-start">
          <h2 class="hero-title m-0">Devotion that never <strong class="fst-italic">ends</strong> </h2>
          <p class="my-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis eligendi laboriosam quae, saepe ratione iure? Laboriosam quae, saepe ratione iure?</p>
          <button class="btn btn-hero my-3">READ MORE</button>
        </div>
        <div class="col hero-img d-flex">
          <img src="@/assets/img/h-2-slider-img-15.png" alt="Slider-1">
          <img src="@/assets/img/h-2-slider-img-16.png" alt="Slider-2">
          <img src="@/assets/img/h-2-slider-img-17.png" alt="Slider-3" class="hero-img-flowers">
        </div>
        <div class="container-chevrons-dots">
          <a href="#" class="chevronLink chevronLink-L"><i class="fa fa-chevron-left" aria-hidden="true"></i></a>
          <a href="#" class="chevronLink chevronLink-R"><i class="fa fa-chevron-right" aria-hidden="true"></i></a>
          <ul class="list-dots d-flex m-0">
            <li class="hero-dot mx-1 p-2"><i class="fa fa-circle" aria-hidden="true"></i></li>
            <li class="hero-dot mx-1 p-2"><i class="fa fa-circle" aria-hidden="true"></i></li>
            <li class="hero-dot hero-dot-active mx-2 p-2"><i class="fa fa-circle" aria-hidden="true"></i></li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {

  },
  data(){
    return {
      logoHeader: 'logo-sidearea-1.png',
      navbarItems: [
        'HOME',
        'PAGES',
        'PORTFOLIO',
        'BLOG',
        'SHOP',
        'ELEMENTS'
      ]
    };
  },
  methods: {

  }
}
</script>

<style lang='scss'>
header{
  position: relative;
  .navbar{
    .img-nav{
      width: 100px;
    }
    ul{

      li{
        img{
          width: 20px;
        }
      }
    }
  }
  .hero{
    max-width: 65%;
    .row{
      
      .hero-text{
            .hero-title{
              font-size: 75px;
            }
            .btn-hero{
              font-size: 11px;
              font-weight: bold;
              border: 2px solid rgb(225, 192, 176);
              padding: 15px 30px;
              border-radius: 0;
            }
      }

      .hero-img{
        position: relative;

        .hero-img-flowers{
          max-height: 30%;
          width: 85px;
          position: absolute;
          bottom: 0;
          right: -85px;
        }
      }

      .container-chevrons-dots{
        background-color: white;

        .chevronLink{
          position: absolute;
          top: 50%;
          transform: translateY(-50%);
          background-color: rgb(225, 192, 176);
          color: white;
          width: 30px;
          height: 30px;
          border-radius: 50%;
          line-height: 32px;

          i{
            &:hover{
            transform: scale(1.3);
          }
          }
        }
        .chevronLink-L{
          left: 0;
        }
        .chevronLink-R{
          right: 0;
        }

        .list-dots{
          color: rgb(225, 192, 176);
          list-style: none;
          position: absolute;
          bottom: -20 px;
          left: 50%;
          transform: translateX(-50%);
          font-size: 10px;

          .hero-dot-active{
            transform: scale(1.4);
          }
        }
      }
    }
  }
}
</style>