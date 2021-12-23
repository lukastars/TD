<template>
  <div class="px-9 sm:px-16 pt-[8rem] pb-16 section" id="section3">
    <h1 class="text-2xl lg:text-3xl text-center font-bold font-serif mb-5">
      Section 3
    </h1>

    <div>
      <Flickity ref="main" :options="mainImgOtions" class="carousel-main">
        <div
          v-for="(image, index) in fullImages"
          :key="index"
          class="carousel-cel p-0 sm:p-12"
        >
          <img
            :key="index"
            :src="image"
            alt="Left image"
            class="rounded-2xl w-full carousel-cell-image min-h-[300px] sm:min-h-[600px]"
          />
        </div>
      </Flickity>

      <Flickity ref="nav" :options="navImgOtions" class="carousel-nav">
        <div
          v-for="(thumbnail, index) in thumbnails"
          :key="index"
          class="carousel-cel p-3"
        >
          <img
            :key="index"
            :src="thumbnail"
            alt="Left image"
            class="rounded-2xl min-h-[150px]"
          />
        </div>
      </Flickity>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import Flickity from 'vue-flickity';
import 'flickity-as-nav-for';
import 'flickity-fade';
export default {
  name: 'SectionThree',
  components: { Flickity },
  data() {
    return {
      loading: true,
      allImages: [],
      fullImages: [''],
      thumbnails: [''],

      mainImgOtions: {
        fade: true,
        imagesLoaded: true,
        contain: true,

        prevNextButtons: false,
        pageDots: false,
      },
      navImgOtions: {
        asNavFor: '.carousel-main',

        contain: true,
        imagesLoaded: true,

        prevNextButtons: false,
        pageDots: false,
      },
    };
  },
  methods: {
    async getImages() {
      try {
        this.loading = true;
        const response = await axios.get(
          'https://jsonplaceholder.typicode.com/photos?albumId=1'
        );

        return response.data;
      } catch (error) {
        console.log(error);
      }
    },

    filterImages() {
      let fullImages = [];
      let thumbnails = [];
      this.allImages.forEach((item) => {
        fullImages.push(item.url);
        thumbnails.push(item.thumbnailUrl);
      });
      this.fullImages = fullImages;
      this.thumbnails = thumbnails;

      setTimeout(() => {
        this.reload();
      }, 1000);
    },
    reload() {
      this.$refs.main.rerender();
      this.$refs.nav.rerender();
    },
  },

  async mounted() {
    const reslults = await this.getImages();
    this.allImages = reslults;
    this.filterImages();
    this.reload();
  },
};
</script>

<style>
.carousel-cell {
  width: 100%;
  height: 300px;
  margin-right: 10px;
  /* center images in cells with flexbox */
  display: flex;
  align-items: center;
  justify-content: center;
}
.carousel-cell-image {
  display: block;
  max-height: 100%;
}
</style>
