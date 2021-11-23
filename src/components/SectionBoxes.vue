<template>
  <div class="sectionBoxes container-fluid">
    <div class="row row-cols-3">
      <div class="col p-0"
        v-for="(boxImg, i) in boxImgList"
        :key="i"
      >
        <img class="w-100" :src='require("@/assets/img/" + boxImg)' :alt='"boxImg" + i'>
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

<style>

</style>