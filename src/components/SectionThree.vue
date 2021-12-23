<template>
  <div class="px-16 pt-[8rem] section" id="section3">
    <h1 class="text-3xl text-center font-bold font-serif mb-5">Section 3</h1>
    <div v-if="loading">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        style="margin: auto; background: #fff; display: block"
        width="200px"
        height="200px"
        viewBox="0 0 100 100"
        preserveAspectRatio="xMidYMid"
      >
        <g transform="rotate(0 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.9166666666666666s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(30 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.8333333333333334s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(60 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.75s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(90 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.6666666666666666s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(120 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.5833333333333334s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(150 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.5s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(180 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.4166666666666667s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(210 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.3333333333333333s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(240 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.25s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(270 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.16666666666666666s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(300 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="-0.08333333333333333s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
        <g transform="rotate(330 50 50)">
          <rect
            x="47"
            y="24"
            rx="3"
            ry="6"
            width="6"
            height="12"
            fill="#044d73"
          >
            <animate
              attributeName="opacity"
              values="1;0"
              keyTimes="0;1"
              dur="1s"
              begin="0s"
              repeatCount="indefinite"
            ></animate>
          </rect>
        </g>
      </svg>
    </div>
    <div>
      <Flickity
        v-if="!loading"
        ref="main"
        :options="mainImgOtions"
        class="carousel-main"
      >
        <div
          v-for="(image, index) in fullImages"
          :key="index"
          class="carousel-cel p-12"
        >
          <img
            :key="index"
            :src="image"
            alt="Left image"
            class="rounded-2xl w-full carousel-cell-image min-h-[600px]"
          />
        </div>
      </Flickity>

      <Flickity
        v-if="!loading"
        ref="nav"
        :options="navImgOtions"
        class="carousel-nav"
      >
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
      loading: false,
      allImages: [],
      fullImages: [],
      thumbnails: [],

      imgVisible: 1,
      mainImgOtions: {
        imagesLoaded: true,
        initialIndex: 1,
        prevNextButtons: false,
        pageDots: false,
      },
      navImgOtions: {
        imagesLoaded: true,
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
        this.loading = true;
        const response = await axios.get(
          'https://jsonplaceholder.typicode.com/photos?albumId=1'
        );
        setTimeout(() => {
          this.loading = false;
        }, 1000);

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
    this.filterImages();
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
