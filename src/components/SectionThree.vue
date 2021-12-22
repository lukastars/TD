<template>
  <div v-if="loading">asddd</div>
  <div v-if="!loading">
    <Flickity ref="main" :options="mainImgOtions" class="carousel-main">
      <div
        v-for="(image, index) in fullImages"
        :key="index"
        class="carousel-cel p-12"
      >
        <img
          :key="index"
          :src="image"
          alt="Left image"
          class="rounded-2xl w-full carousel-cell-image"
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
          class="rounded-2xl"
        />
      </div>
    </Flickity>
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
      fullImages: [
        'https://via.placeholder.com/600/92c952',
        'https://via.placeholder.com/600/92c952',
        'https://via.placeholder.com/600/92c952',
      ],
      thumbnails: [
        'https://via.placeholder.com/150/92c952',
        'https://via.placeholder.com/150/92c952',
        'https://via.placeholder.com/150/92c952',
      ],

      imgVisible: 0,
      mainImgOtions: {
        fade: true,
        imagesLoaded: true,
        initialIndex: 0,
        prevNextButtons: false,
        pageDots: false,
      },
      navImgOtions: {
        asNavFor: '.carousel-main',
        freeScroll: false,
        contain: true,
        prevNextButtons: false,
        pageDots: false,
      },
    };
  },
  methods: {
    async getImages() {
      try {
        const response = await axios.get(
          'https://jsonplaceholder.typicode.com/photos?albumId=1'
        );
        this.loading = false;
        return response.data;
      } catch (error) {
        console.log(error);
      }
    },

    filterImages() {
      this.allImages.forEach((item) => {
        this.fullImages.push(item.url);
        this.thumbnails.push(item.thumbnailUrl);
      });
    },
  },

  async mounted() {
    this.allImages = await this.getImages();
    await this.filterImages();
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
