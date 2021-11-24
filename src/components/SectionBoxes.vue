<template>
  <div class="sectionBoxes container-fluid">
    <div class="row row-cols-3">
      <div class="col p-0"
        v-for="(boxImg, i) in boxImgList"
        :key="i"
      >
        <img class="w-100" :src='require("@/assets/img/" + boxImg)' :alt='"boxImg" + i'>
        <div class="overlayBox p-4" :class="(i=== 3) ? 'overlayBox-active' : ''">
          <h2 class="fs-3">Illustrations of novels</h2>
          <h6 class="fst-italic m-0">Illustration</h6>
        </div>
      </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: "SectionBoxes",
  props: {

  },
  data() {
    return {
      boxImgList: [
        "h-2-port-img-1.jpg",
        "h-2-port-img-2.jpg",
        "h-2-port-img-3.jpg",
        "h-2-port-img-4.jpg",
        "h-2-port-img-5.jpg",
        "h-2-port-img-6.jpg",
      ]
    };
  },
}
</script>

<style lang='scss'>
.sectionBoxes{
  .row{
    .col{
      position: relative;

      .overlayBox{
        position: absolute;
        background: white;
        top: 50%;
        left: 0;
        transform: translateY(-50%);
        text-align: start;
        opacity: 0;
      }

      &:hover{
        .overlayBox-active{
        opacity: 1;
        transition: opacity .6s;
        }
      }
    }
  }
}
</style>