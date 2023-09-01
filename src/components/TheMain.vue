<script>
import Slider from "./Slider.vue"
export default {
  components: {
    Slider
  },
  data() {
    return {
      img: [
        "choco-chip-cookies.jpg",
        "strawberry-jam-cookies.jpg",
        "cookies-with-ice-cream.jpg",
        "home-bread.jpg"
      ]
    }
  }
}
</script>

<template>
  <main>
    <!-- Prima Sezione - OUR PRODUCTS -->
    <section>
      <div class="container d-flex justify-content-between">
        <div class="col-4 ">
          <span>OUR PRODUCTS</span>
          <h2>All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural, all
            organic ingredients.</h2>
          <button>Buy Avada Today!</button>
        </div>
        <Slider :carouselSlide="2" :img="img" />
      </div>
    </section>

  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

section {
  padding: 4rem 0;
}

h2 {
  color: $color-primary;
  font-weight: 600;
}

button {
  border: 0;
  border-radius: 6px;
  padding: .5rem 1rem;
  background-color: $color-primary;
  color: white;

  &:hover {
    background-color: white;
    color: $color-primary;
    border: 1px solid #f0edf5;
  }
}
</style>
