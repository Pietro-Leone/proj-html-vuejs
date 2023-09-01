<script>
export default {
  props: {
    img: Array,
    carouselSlide: Number
  }
}
</script>

<template>
  <div id="carousel" class="carousel slide w-50">
    <div class="carousel-inner">
      <div class="carousel-item" :class="i === 0 ? 'active' : ''" v-for="(el, i) in carouselSlide">
        <div class="d-flex gap-3">
          <img :src="`src/assets/${[img[i]]}`" class="d-block w-100" alt="img">
          <img :src="`src/assets/${img[i+2]}`" class="d-block w-100" alt="img">
        </div>
      </div>
    </div>
    <button class="carousel-control-prev" type="button" data-bs-target="#carousel" data-bs-slide="prev">
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#carousel" data-bs-slide="next">
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