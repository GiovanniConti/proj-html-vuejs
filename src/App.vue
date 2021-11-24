<template>
  <div id="app">
    <Header></Header>
    <Main></Main>
    <Footer></Footer>
    <Overlay></Overlay>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Overlay from './components/Overlay.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Overlay,

  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;0,800;0,900;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
@import '@/styles/app.scss';

#app {
  text-align: center;
  font-family: 'Playfair Display', serif;
}
</style>
