<template>
  <header class="m-4">
    <div class="navbar p-0">
      <!-- logo Nav -->
      <img :src="require('@/assets/img/' + logoHeader)" alt="Logo Header" class="img-nav">
      <!-- Nav List -->
      <ul class="navList list-inline m-0 fw-bold">
        <li
          class="list-inline-item mx-3 px-1"
          v-for="(item, i) in navbarItems"
          :key="i"
          @click= 'onNavItemClick(i)'
          :class="(navItemActive === i) ? 'navItem-Active' : ''" 
        >{{ item }}</li>
        <li class="list-inline-item ms-4">
          <img src="@/assets/svg/svg-1.svg" alt="svg-navbar">
          </li>
      </ul>
    </div>
    <!-- Section HERO (Carosel) -->
    <div class="hero container-xl py-5 px-0">
      <div class="row py-5">
        <!-- Container Hero Text (L) -->
        <div class="col hero-text text-start">
          <h2 class="hero-title m-0">Devotion that never <strong class="fst-italic">ends</strong> </h2>
          <p class="my-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Blanditiis eligendi laboriosam quae, saepe ratione iure? Laboriosam quae, saepe ratione iure?</p>
          <button class="btn btn-hero my-3">READ MORE</button>
        </div>
        <!-- Container Hero Img (R) -->
        <div class="col hero-img">
          <img src="@/assets/img/hero-img.jpg" alt="Slider-1" class="img-fluid">
        </div>
        <!--
        <div class="col hero-img d-flex p-0">
          <img src="@/assets/img/h-2-slider-img-15.png" alt="Slider-1">
          <img src="@/assets/img/h-2-slider-img-16.png" alt="Slider-2">
          <img src="@/assets/img/h-2-slider-img-17.png" alt="Slider-3" class="hero-img-flowers">
        </div>
        -->
        <!-- Carosel overlay elements -->
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
        'ELEMENTS',
        // '<img src="@/assets/svg/svg-1.svg" alt="svg-navbar">'
      ],
      navItemActive: 0,
    };
  },
  methods: {
    onNavItemClick(el) {
      this.navItemActive = el;
    }
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
      font-size: 12px;

      li{
        cursor: pointer;
        letter-spacing: 5px;

        img{
          width: 20px;
        }
      }

      .navItem-Active{
        background: linear-gradient(0deg, rgb(239, 205, 190) 30%, white 50%);
        line-height: 15px;
      }
    }
  }
  .hero{
    // max-width: 65%;
    .row{
      
      .hero-text{
            .hero-title{
              font-size: 75px;
            }

            p{
              color: #878787;
            }
            .btn-hero{
              font-size: 11px;
              font-weight: bold;
              border: 2px solid #E1C0B0;
              padding: 15px 30px;
              border-radius: 0;
              box-shadow: none;
              letter-spacing: 5px;
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
        cursor: pointer;

        .chevronLink{
          position: absolute;
          top: 50%;
          transform: translateY(-50%);
          background-color: #E1C0B0;
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
          color: #E1C0B0;
          list-style: none;
          position: absolute;
          bottom: 0;
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