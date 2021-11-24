<template>
  <div class="overlay">
    <div class="containerTop">
      <img src="@/assets/svg/svg-4.svg" alt="related" class="overlay_icon related">
      <img src="@/assets/svg/svg-6.svg" alt="cart" class="overlay_icon cart">
    </div>
    <img src="@/assets/svg/svg-2.svg" alt="backToTop" class="overlay_icon backToTop">
  </div>
</template>

<script>
export default {
  name: 'Overlay',
  data(){
    return{

    };
  },
}
</script>

<style lang="scss">
  .containerTop{
    display: flex;
    flex-direction: column;
    position: fixed;
    top: 20%;
    right: 0;
  }

  .overlay_icon{
    width: 45px;
    height: 45px;
    padding: 10px;
    background: red;
  }

  .cart{
    background: white;
    margin-top: 8px;
  }

  .backToTop{
    position: fixed;
    bottom: 1%;
    right: 1%;
    background: #C0E1CF;
  }
</style>