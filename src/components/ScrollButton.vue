<script>
export default {
  props: {
    N: Number,
    icon: String,
    title: String,
  }
}
</script>

<template>
  <div class="button-icon d-flex flex-column" :style="`top: calc(150px + (70px * ${N}))`">
    <div class="d-flex position-relative" style="height: 32px; aspect-ratio: 1/1;">
      <i :class="`i-after ${icon}`"></i>
      <i :class="`i-before ${icon}`"></i>

    </div>
    <span class="title-button">{{title}}</span>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

.button-icon {
  width: 66px;
  aspect-ratio: 1/1;
  justify-content: center;
  align-items: center;
  position: absolute;
  border-radius: 6px;
  right: 15px;
  color: #33475b;
  background-color: white;
  box-shadow: 0 -5px 20px 5px rgba(0, 0, 0, .15);
  overflow: hidden;

  span {
    font-size: 12px;
    font-weight: 700;
  }

  i {
    font-size: 24px;
    position: absolute;

  }

  .i-before {
    transition: opacity .4s cubic-bezier(.21, .6, .35, 1), width .4s cubic-bezier(.21, .6, .35, 1), height .4s cubic-bezier(.21, .6, .35, 1), transform .2s cubic-bezier(.21, .6, .35, 1);
  }

  .i-after {
    transition: opacity .4s cubic-bezier(.21, .6, .35, 1), width .4s cubic-bezier(.21, .6, .35, 1), height .4s cubic-bezier(.21, .6, .35, 1), transform .2s cubic-bezier(.21, .6, .35, 1);
    transform: translateX(60px);

  }

  &:hover {
    .i-before {
      transform: translateX(-60px);
    }

    .i-after {
      transform: translateX(0);
    }
  }
}
</style>