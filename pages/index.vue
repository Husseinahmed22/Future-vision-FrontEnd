<template>
  <div>
    <header class="uni-info-pageheader">
      <navbar />

      <div class="container-fluid pr-5 pl-5">
        <div class="row">
          <div class="col-md-6" style="margin-top: 180px">
            <p class="uni-info-pageheader-text mt-5">
              <span>Welcome to Future Vision ..</span> <br />
              Where we will help you find out the the college that suits your
              interests. Answer some few questions and let the rest for us.
            </p>
            <nuxt-link to="/login" class="btn main-login">Login</nuxt-link>
            <div>
              <nuxt-link to="/signup" class="btn main-signup"
                >Sign up</nuxt-link
              >
            </div>
          </div>
          <div class="col-md-6" style="margin-top: 150px">
            <div class="row">
              <div class="col-md-7">
                <img
                  src="../assets/images/russian.png"
                  class="uni-info-pageheader-img"
                  alt=""
                />
              </div>
              <div class="col-md-5 pt-5">
                <img
                  src="../assets/images/alamin.png"
                  class="uni-info-pageheader-img"
                  alt=""
                />
              </div>
            </div>
            <div class="row">
              <div class="col-md-5 pt-5">
                <img
                  src="../assets/images/stud.png"
                  class="uni-info-pageheader-img"
                  alt=""
                />
              </div>
              <div class="col-md-7">
                <img
                  src="../assets/images/hoaras.png"
                  class="uni-info-pageheader-img"
                  alt=""
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </header>

    <section class="uni-main" id="universities">
      <div class="uni-layer">

         </div>
        <slider />

      
    </section>
  </div>
</template>
<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import Slider from '~/components/slider.vue';
import navbar from "../components/navbar.vue";
export default {
  components: { navbar, Slider },
  name: "MyComponent",
  
};
</script>
<style></style>
