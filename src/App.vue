<script>
import Header from "./components/TheHeader.vue"
import Main from "./components/TheMain.vue"
import Footer from "./components/TheFooter.vue"
import ScrollButton from "./components/ScrollButton.vue"
export default {
  components: {
    Header,
    Main,
    Footer,
    ScrollButton,
  }
}
</script>

<template>
  <div class="scroll-fixed">
    <ScrollButton :N="0" :icon="'fa-solid fa-dragon'" :title="'Prebuilts'" />
    <ScrollButton :N="1" :icon="'fa-solid fa-cart-shopping'" :title="'Buy Now'" />
  </div>
  <Header />
  <Main />
  <Footer />
</template>

<style lang="scss">
.scroll-fixed {
  position: fixed;
  right: 0;
  top: 0;
  z-index: 2;
}
</style>
