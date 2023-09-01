<script>
import Nav from "./Nav.vue"
import Jumbotron from "./Jumbotron.vue"
export default {
  components: {
    Nav,
    Jumbotron,
  },
  data(){
    return{
      navElements:[
        'shop',
        'about',
        'gallery',
        'location',
        'journal',
        'contact'
      ]
    }
  }
}
</script>

<template>
  <header>
    <div class="shipping">Free International Shipping - 10% OFF SITE</div>
    <Nav :navElements="navElements"/>
    <Jumbotron/>
  </header>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

header{
  background-image: url("../assets/hero-header-bakery.jpg");
  background-position: center;
  background-size: cover;
  background-size: 150%;
  background-repeat: no-repeat;
  .shipping{
    text-align: center;
    background-color: white;
    color: $color-primary;
    padding: .5rem 0;
  }
}
</style>
