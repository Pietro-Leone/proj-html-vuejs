<script>
import List from "./List.vue"
export default {
  components: {
    List
  },
  data() {
    return {
      navElements: [
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
  <div class="container pb-5">
    <div class="row">
      <div class="col">
        <img src="../assets/avada-bakery-logo.png" alt="logo">
        <div class="py-3">
          <List :navElements="navElements" />
        </div>
        <span class="copyright">© Copyright 2023 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by
          Boolean</span>
      </div>
      <div class="col">
        <h3>Subscribe to our Newsletter</h3>
        <div>
          <form class="row py-3 g-3">
            <div class="col-9">
              <label for="input" class="visually-hidden">email</label>
              <input type="email" class="form-control" id="input" placeholder="enter email address*">
            </div>
            <div class="col-3">
              <button type="submit" class="btn btn-primary mb-3 w-100">Sunscribe</button>
            </div>
          </form>
        </div>
        <div class="social">
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
          <a href="#"><i class="fa-brands fa-x-twitter"></i></a>
          <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="#"><i class="fa-brands fa-pinterest-p"></i></a>
          <a href="#"><i class="fa-brands fa-youtube"></i></a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

h3 {
  color: $color-primary;
  font-weight: 600;
}

input {
  height: 48px;
}

button {
  border: 0;
  border-radius: 6px;
  padding: .5rem 1rem;
  background-color: $color-primary;
  color: white;
  height: 48px;

  &:hover {
    background-color: white;
    color: $color-primary;
    border: 1px solid #f0edf5;
  }
}

.copyright {
  font-size: 12px;
  color: #676371;
}

.social {
  display: flex;
  justify-content: flex-end;

  a {
    padding: 8px;
    margin: 5px;
    color: $color-primary;
  }
}
</style>
