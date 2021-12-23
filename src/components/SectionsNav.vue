<template>
  <div class="menu w-full z-10">
    <div class="flex justify-around text-sm md:text-md lg:text-lg">
      <a
        href="#section1"
        v-on:click="setActive('section1')"
        :class="[
          isActive('section1')
            ? 'text-center border-b-4 border-[#044D73] text-[#044D73]  py-3 md:py-6 bg-white w-full font-sans font-bold '
            : 'text-center text-[#585f65] py-3 md:py-6 bg-white w-full font-sans font-bold ',
        ]"
      >
        Section 1
      </a>
      <a
        href="#section2"
        v-on:click="setActive('section2')"
        :class="[
          isActive('section2')
            ? 'text-center border-b-4 border-[#044D73] text-[#044D73] py-3 md:py-6 bg-white w-full font-sans font-bold '
            : 'text-center text-[#585f65] py-3 md:py-6 bg-white w-full font-sans font-bold ',
        ]"
      >
        Section 2
      </a>
      <a
        href="#section3"
        v-on:click="setActive('section3')"
        :class="[
          isActive('section3')
            ? 'text-center border-b-4 border-[#044D73] text-[#044D73] py-3 md:py-6 bg-white w-full font-sans font-bold '
            : 'text-center text-[#585f65] py-3 md:py-6 bg-white w-full font-sans font-bold ',
        ]"
      >
        Section 3
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SectionsNav',
  data() {
    return {
      activeTab: 'section1',
    };
  },
  methods: {
    setActive(name) {
      this.activeTab = name;
    },
    isActive(name) {
      return this.activeTab === name;
    },
    trackScroll() {
      let num = window.innerHeight / 2;
      window.addEventListener('scroll', () => {
        if (window.scrollY > num) {
          document.querySelector('.menu').classList.add('fixed');
        } else {
          document.querySelector('.menu').classList.remove('fixed');
        }

        const sections = document.querySelectorAll('.section');

        sections.forEach((section) => {
          const sectionTop = section.offsetTop;
          if (scrollY >= sectionTop) {
            this.activeTab = section.getAttribute('id');
          }
        });
      });
    },
  },
  created() {
    this.trackScroll();
  },
};
</script>

<style>
.menu {
  position: absolute;
}
.fixed {
  position: fixed;
  top: 0;
}
</style>
