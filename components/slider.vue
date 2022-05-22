<template v-slot:activator="{ on, attrs }">
  <div>
         <VueSlickCarousel v-bind="slickOptions2" ref="carousel">
          <div
          style="height: 100%"
        v-for="list in lists.data"
        :key="list.index"
        >
        <div class="container uni-con">
            <div class="row uni-row" style="margin-top: 180px">
              <div class="col-md-6">
                <div class="uni-img">
                  <img src="../assets/images/alamin.png" alt="" />
                </div>
              </div>
              <div class="col-md-6 mt-5">
                <h1 class="uni-name">{{ list.name }}</h1>
                <h1 class="uni-name">University</h1>
                <div class="college-slide">
                  <VueSlickCarousel v-bind="slickOptions">
                    <div>faculty of nursing</div>
                    <div>faculty of engineering</div>
                    <div>faculty of medicine</div>
                    <div>faculty of culture</div>
                  </VueSlickCarousel>
                </div>
                <div class="location">
                  <img
                    src="../assets/images/Path 5.png"
                    alt=""
                    style="display: inline-block"
                  />
                  <span>{{ list.location }}</span>
                </div>
              </div>
            </div>  
        </div>
        
        </div>
        
        </VueSlickCarousel>
  </div>
</template>
<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
  export default {
      components: {  VueSlickCarousel },
  data() {
    return {
      lists: [],
       slickOptions:{
           autoplay:true,
            autoplaySpeed:1500
       },
      slickOptions2: {
        arrows: true,
        dots: true,
      },
    };
  },
  async fetch() {
    await this.getuniversities();
  },
  methods: {
    async getuniversities() {
      const unversity = this.$axios.get("/list");
      this.lists = await unversity;
      console.log(this.lists);
    },
  },
  }
</script>
<style>

</style>
