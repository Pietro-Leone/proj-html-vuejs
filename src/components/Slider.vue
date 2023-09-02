<script>
export default {
  props: {
    img: Array,
    carouselSlide: Number,
  },
  data() {
    return {
      currentIndex: 0,
    }
  },
  computed: {
    totalSlides() {
      return Math.ceil(this.img.length / this.carouselSlide);
    },
    currentSlideImages() {
      const start = this.currentIndex * this.carouselSlide;
      const end = start + this.carouselSlide;
      return this.img.slice(start, end);
    },
  },
  methods: {
    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.totalSlides;
    },
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1 + this.totalSlides) % this.totalSlides;
    },
  }
}
</script>

<template>
  <div :id="`carousel`" class="carousel slide">
    <div class="carousel-inner">
      <div class="carousel-item" :class="{ active: i === currentIndex }" v-for="(slideImages, i) in carouselSlide"
        :key="index">
        <div class="d-flex gap-3">
          <img :src="`src/assets/${image}`" class="d-block w-100" alt="img"
            v-for="(image, imageIndex) in currentSlideImages" :key="imageIndex">
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" @click="prevSlide">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" @click="nextSlide">
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Next</span>
    </button>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.carousel-control-prev,
.carousel-control-next {
  height: 25%;
  width: 8%;
  background-color: $color-primary;
  margin-top: auto;
  margin-bottom: auto;
}
</style>