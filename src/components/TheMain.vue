<script>
import Slider from "./Slider.vue"
export default {
  components: {
    Slider,
  },
  data() {
    return {
      firstCarousel: [
        "choco-chip-cookies.jpg",
        "strawberry-jam-cookies.jpg",
        "cookies-with-ice-cream.jpg",
        "home-bread.jpg"
      ],
      secondCarousel: [
        "choco-chip-cookies.jpg",
        "strawberry-jam-cookies.jpg",
        "strawberry-donut.jpg",
        "perfect-macarons.jpg",
        "premium-bread.jpg",
        "cherry-cake.jpg",
        "cookies-with-ice-cream.jpg",
        "blackberry-stuffed-bread.jpg",
        "glazed-pancake-with-lemon.jpg",
        "small-cupcake.jpg",
        "home-bread.jpg",
        "choco-chip-cookies.jpg"
      ],
      wedding: true,
      corporate: true,
    }
  }
}
</script>

<template>
  <main>
    <!-- Prima Sezione - OUR PRODUCTS -->
    <section>
      <div class="container d-flex justify-content-between">
        <div class="row">
          <div class="col-4 ">
            <span class="text-uppercase">Our Products</span>
            <h2>All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural,
              all
              organic ingredients.</h2>
            <button>Buy Avada Today!</button>
          </div>
          <div class="col-8">
            <Slider :carouselSlide="2" :img="firstCarousel" :px="530"  />
          </div>
        </div>
      </div>
    </section>
    <!-- Seconda Sezione - Corporate & Weddings -->
    <section>
      <div class="container text-center">
        <span class="text-uppercase">Corporate & Weddings</span>
        <h2>Baking Special Moments</h2>
        <div class="row">
          <div class="col-6">
            <div class="corporate-wedding" @mouseover="corporate = false" @mouseleave="corporate = true">
              <div class="position-relative">
                <img src="../assets/corporate-bg.jpg" alt="img" v-if="corporate">
                <img src="../assets/corporate-hover-bg.jpg" alt="img" v-if="!corporate">
              </div>
              <div class="position-absolute">
                <span class="text-uppercase">International Bakery</span>
                <h2>Corporate Events</h2>
                <div><button>Explore more</button></div>
              </div>
            </div>
          </div>
          <div class="col-6">
            <div class="corporate-wedding" @mouseover="wedding = false" @mouseleave="wedding = true">
              <img src="../assets/wedding-bg.jpg" alt="img" v-if="wedding">
              <img src="../assets/wedding-hover-bg.jpg" alt="img" v-if="!wedding">
              <div class="position-absolute">
                <span class="text-uppercase">Private Dining Hall</span>
                <h2>Weddings & Parties</h2>
                <div><button>Explore more</button></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Terza Sezione - OUR PRODUCTS -->
    <section>
      <div class="container d-flex justify-content-between">
        <div class="row">
          <div class="col-3 text-center">
            <h2>Find a freshly baked product perfect for you</h2>
            <p>Integer a nibh vitae ex porttitor rutrum et ut velit. Etiam ac felis at leo feugiat placerat. Sed ac nulla
              id
              orci tempor convallis sed.</p>
            <button>Shop All Products</button>
          </div>
          <div class="col-9">
            <Slider :carouselSlide="4" :img="secondCarousel" :px="250" />
          </div>
        </div>
      </div>
    </section>
    <!-- Quarta Sezione -->
    <section>
      <div class="container">
        <div class="row">
          <div class="col">
            <div class="bakery-process bakery-process-1 p-5">
              <h2 class="display-4">Tell us what you have in mind</h2>
              <div class="d-flex flex-column justify-content-between" style="width: 30%;">
                <p class="number">01</p>
                <p>Manual Ingredients Selection <br><br>
                  <span>Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu laoreet ex.
                    Aliquam erat
                    volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec lorem erat,
                    finibus
                    in velit placerat, rutrum augue.</span>
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col">
            <div class="bakery-process bakery-process-2 p-5">
              <div class="d-flex flex-column justify-content-between" style="width: 50%;">
                <h2 class="display-4">We Start Baking</h2>
                <p>Sweet & Delicious<br><br>
                  <span>Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu laoreet ex.
                    Aliquam erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec
                    lorem erat, finibus in velit placerat.</span>
                </p>
              </div>
              <p class="number">02</p>
            </div>
          </div>
          <div class="col">
            <div class="bakery-process-text w-100 h-100 p-5">
              <div class="fs-5">Dont Just Take Our WOrd For it</div>
              <h2 style="font-size: 3.5rem; font-weight: bold;">“Finally found an alternative to the mass produced
                products. Something that
                incorporates real organic
                ingredients, nutrient dense wellness while promoting sustainability and activity.”</h2>
              <div class="fs-5">Rachel Cooper, Founder</div>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col">
            <div class="bakery-process bakery-process-3 p-5">
              <div class="d-flex flex-column justify-content-between" style="width: 50%;">
                <h2 class="display-4">Delivered to your home</h2>
                <p>Baked to Order & Gift Wrapped<br><br>
                  <span>Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl varius. Ut eu laoreet ex.
                    Aliquam erat volutpat. Nullam quis sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec
                    lorem erat, finibus in velit placerat, rutrum augue.</span>
                </p>
              </div>
              <p class="number">03</p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Quinta Sezione - Location -->
    <section>
      <div class="container text-center locations">
        <span class="text-uppercase">Locations</span>
        <h2>Visit our Bakeries</h2>

        <div class="row">
          <div class="ms-col">
            <div class="overflow-hidden">
              <img src="../assets/new-york-bk.jpg" alt="location">
            </div>
            <div class="row">
              <h2>New York</h2>
              <div class="col">
                <div>CALL US</div>
                <div>1.800.458.556</div>
              </div>
              <div class="col">
                <div>OPEN ALL WEEK</div>
                <div>9:00 AM - 6:00 PM</div>
              </div>
              <div class="col">
                <button>View Map</button>
              </div>
            </div>
          </div>
          <div class="ms-col">
            <div class="overflow-hidden">
              <img src="../assets/london-bk.jpg" alt="location">
            </div>
            <div class="row">
              <h2>London</h2>
              <div class="col">
                <div>CALL US</div>
                <div>1.800.458.556</div>
              </div>
              <div class="col">
                <div>OPEN ALL WEEK</div>
                <div>9:00 AM - 6:00 PM</div>
              </div>
              <div class="col">
                <button>View Map</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Sesta Sezione -->
    <section>
      <div class="container social">
        <div class="row justify-content-between">
          <div class="col-3">
            <div class="overflow-hidden"><img src="../assets/social-1.jpg" alt="location"></div>
          </div>
          <div class="col-5">
            <div class="follow-us">
              <div class="text-center">
                <p>Made for Sharing</p>
                <h2> Let's stay in touch </h2>
                <button><i class="fa-brands fa-instagram"></i> Follow Us</button>
              </div>
            </div>
          </div>
          <div class="col-3">
            <div class="overflow-hidden"><img src="../assets/social-2.jpg" alt="location"></div>
          </div>
        </div>
        <div class="row justify-content-between">
          <div class="col-3">
            <div class="overflow-hidden"><img src="../assets/social-3.jpg" alt="location"></div>
          </div>
          <div class="col-3">
            <div class="overflow-hidden"><img src="../assets/social-4.jpg" alt="location"></div>
          </div>
          <div class="col-3">
            <div class="overflow-hidden"><img src="../assets/social-5.jpg" alt="location"></div>
          </div>
          <div class="col-3">
            <div class="overflow-hidden"><img src="../assets/social-6.jpg" alt="location"></div>
          </div>
        </div>
      </div>
    </section>
    <!-- Settima Sezione -->
    <section>
      <div class="try-products">
        <div class="container">
          <div class="row">
            <div class="col">
              <div class="d-flex align-items-center">
                <div style="width: 600px;">
                  <p>Try our Seasonal Products</p>
                  <h2 class="display-4 my-3">Order for pick-up or delivery to your home</h2>
                  <button>Shop Now</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

section {
  padding: 4rem 0;

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

  img {
    width: 100%;
  }
}

.corporate-wedding {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;

  img{
    position: relative;
  }

  h2,
  span {
    color: white;
  }

  .position-absolute {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
    height: 100%;
    opacity: 0;

    &:hover {
      transition: opacity 1s;
      opacity: 1;
    }
  }
}

.row {
  margin-top: 2rem;
}

.bakery-process {
  background-repeat: no-repeat;
  height: 800px;
  display: flex;
  justify-content: space-between;
  color: white;


  h2 {
    color: white;
    width: 400px;
  }

  p {
    height: min-content;

    span {
      font-size: 1.2rem;
      font-weight: 600;
    }
  }

  p.number {
    width: 100%;
    height: min-content;
    text-align: end;
    font-size: 6rem;
  }

  &.bakery-process-1 {
    background-image: linear-gradient(170deg, hsla(257, 7%, 42%, 40%) 0%, hsla(264, 47%, 37%, 80%) 100%), url("../assets/bakery-process-1.jpg");
  }

  &.bakery-process-2 {
    background-image: linear-gradient(200deg, hsla(257, 7%, 42%, 20%) 0%, #676371 100%), url("../assets/bakery-process-2.jpg");
    background-position: right;
    min-height: 800px;
    height: 100%;
  }

  &.bakery-process-3 {
    background-image: linear-gradient(200deg, rgba(35, 33, 37, 0) 10%, hsla(264, 47%, 37%, 80%) 100%), url("../assets/bakery-process-3.jpg");
    background-position: center;
  }

}

.bakery-process-text {
  background-color: #f0edf5;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.ms-col {
  padding: 0 0 3rem 0;
  background-color: #f0edf5;
  flex-basis: calc(100% / 2);
}

.locations {

  img {
    transition: 1s scale;

    &:hover {
      scale: 1.1;
    }
  }

  button {
    background-color: white;
    color: $color-primary;

    &:hover {
      background-color: $color-primary;
      color: white;
    }
  }
}

.social {

  .col-3,
  .col-5 {
    >div {
      height: 350px;
    }

    img {
      height: 100%;
      object-fit: cover;
      transition: 1s;

      &:hover {
        scale: 1.1;
      }
    }

    .follow-us {
      background-color: #f6f0f3;
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
    }
  }
}

.try-products {
  background-image: url("../assets/call-to-action-bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  height: 470px;
  padding: 2rem 0;
  color: white;

  h2 {
    color: white;
  }

  button {
    background-color: white;
    color: $color-primary;

    &:hover {
      background-color: $color-primary;
      color: white;
    }
  }
}
</style>
