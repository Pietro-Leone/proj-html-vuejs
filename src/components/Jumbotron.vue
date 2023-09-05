<script>
export default {
}
</script>

<template>
  <div class="container p-5">
    <div class="jumbotron my-5 py-5" style="width: 360px;">
      <h6 class="mt-5">Fresh & Tasty Bakery every day</h6>
      <h1 class="display-4">The Perfect Fresh Bread</h1>
      <p class="lead">Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Aliquam erat volutpat.
        Nullam quis sagittis nibh ac nulla id orci tempor.</p>
      <p class="lead">
        <button>Explore our products</button>
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

h6{
  font-size: 12px;
}

h1 {
  color: $color-primary;
  font-weight: bold;
}

button {
  border: 0;
  border-radius: 6px;
  padding: .5rem 1rem;
  background-color: white;
  color: $color-primary;
  &:hover{
    background-color: $color-primary;
    color: white;
  }
}
</style>
