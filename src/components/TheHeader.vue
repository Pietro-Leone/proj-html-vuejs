<script>
import Nav from "./Nav.vue"
export default {
  components: {
    Nav,
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
    <Nav :navElements="navElements" />
  </header>
</template>

<style lang="scss" scoped></style>
