<script>
export default {
  components: {},
  props: {
    navElements: {
      type: Array,
      required: true,
    }
  }
}
</script>

<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container">

      <!-- Left-Nav -->
      <a class="navbar-brand" href="#">
        <img src="/avada-bakery-logo.png" alt="Bootstrap" width="160">
      </a>

      <!-- Center-Nav  -->
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse justify-content-center" id="navbarNav">
        <ul class="navbar-nav">

          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
              aria-expanded="false">home</a>
            <ul class="dropdown-menu border-0">
              <li><a class="dropdown-item" href="#">Classic Shop</a></li>
              <li><a class="dropdown-item" href="#">Extended Width</a></li>
            </ul>
          </li>

          <li class="nav-item" v-for="element in navElements">
            <a class="nav-link" href="#">{{ element }}</a>
          </li>
        </ul>
      </div>

      <!-- Right-Nav -->
      <ul class="navbar-nav">

        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
            aria-expanded="false">account</a>
          <ul class="dropdown-menu dropdown-menu-lg-end border-0" style="width: 280px;">

            <form class="px-4 py-2">
              <div class="mb-2">
                <input type="text" class="form-control" placeholder="Username">
              </div>
              <div class="mb-2">
                <input type="password" class="form-control" placeholder="Password">
              </div>
              <div class="mb-2">
                <div class="form-check">
                  <input type="checkbox" class="form-check-input" id="dropdownCheck">
                  <label class="form-check-label" for="dropdownCheck">Remember me</label>
                </div>
              </div>
              <div class="text-end">
                <button type="submit" class="btn btn-primary">Log in</button>
              </div>
            </form>

          </ul>
        </li>

        <li class="nav-item">
          <a class="nav-link" href="#">
            <i class="fa-solid fa-cart-shopping"></i>
          </a>
        </li>
      </ul>

    </div>
  </nav>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
.nav-link {
  text-transform: uppercase;
  color: $color-primary;
  font-weight: 500;
}

.dropdown-toggle {
  &::after {
    display: none;
  }
}
</style>
