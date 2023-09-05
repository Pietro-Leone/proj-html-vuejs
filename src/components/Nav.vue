<script>
import List from "./List.vue"
export default {
  components: {
    List,
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
      ],
      Sticky: false,
    }
  },
  //
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.Sticky = window.scrollY > 45;
    },
  }


}
</script>

<template>
  <nav class="navbar-expand-lg" :class="{ 'navbar': true, 'sticky': Sticky }">
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
            <a class="home nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
              aria-expanded="false">
              <span class="underline-home"></span>
              home
            </a>
            <ul class="dropdown-menu border-0">
              <li><a class="dropdown-item" href="#">Classic Shop</a></li>
              <li><a class="dropdown-item" href="#">Extended Width</a></li>
            </ul>
          </li>

          <List :navElements="navElements" />

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

nav {
  background-color: transparent;
  padding: 20px;
  position: sticky;
  width: 100%;
  top: 20px;
  z-index: 100;

  &.sticky {
    background-color: white;
    top: 0;
  }
}

.underline-home {
  position: absolute;
  left: 8px;
  top: 40px;
  width: calc(100% - 16px);
  height: 2px;
  background: $color-primary;
  z-index: 30;
}


.nav-link {
  text-transform: uppercase;
  color: $color-primary;
  font-weight: 500;
  position: relative;

  &:hover {
    color: $color-primary;
  }
}

.dropdown-toggle {
  &::after {
    display: none;
  }
}
</style>