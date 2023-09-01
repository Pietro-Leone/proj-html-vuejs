<script>
export default {
}
</script>

<template>
  <div class="container">
    <div class="jumbotron p-4" style="width: 360px;">
      <h6>Fresh & Tasty Bakery every day</h6>
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
