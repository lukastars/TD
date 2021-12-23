<template>
  <div class="menu w-full z-10">
    <div class="flex justify-around">
      <a
        href="#section1"
        v-on:click="setActive('section1')"
        :class="[
          isActive('section1')
            ? 'text-center border-b-4 border-[#044D73] text-[#044D73] py-6 bg-white w-full font-sans font-bold text-lg'
            : 'text-center text-[#585f65] py-6 bg-white w-full font-sans font-bold text-lg',
        ]"
      >
        Section 1
      </a>
      <a
        href="#section2"
        v-on:click="setActive('section2')"
        :class="[
          isActive('section2')
            ? 'text-center border-b-4 border-[#044D73] text-[#044D73] py-6 bg-white w-full font-sans font-bold text-lg'
            : 'text-center text-[#585f65] py-6 bg-white w-full font-sans font-bold text-lg',
        ]"
      >
        Section 2
      </a>
      <a
        href="#section3"
        v-on:click="setActive('section3')"
        :class="[
          isActive('section3')
            ? 'text-center border-b-4 border-[#044D73] text-[#044D73] py-6 bg-white w-full font-sans font-bold text-lg'
            : 'text-center text-[#585f65] py-6 bg-white w-full font-sans font-bold text-lg',
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
      console.log(this.activeTab);
    },
    isActive(name) {
      return this.activeTab === name;
    },
  },
  created() {
    let num = window.innerHeight / 2;

    window.addEventListener('scroll', () => {
      if (window.scrollY > num) {
        document.querySelector('.menu').classList.add('fixed');
      } else {
        document.querySelector('.menu').classList.remove('fixed');
      }
    });

    const sections = document.querySelectorAll('.section');

    window.onscroll = () => {
      sections.forEach((section) => {
        const sectionTop = section.offsetTop;
        if (scrollY >= sectionTop) {
          setTimeout(() => {
            this.activeTab = section.getAttribute('id');
          }, 100);
        }
      });
    };
  },
};
</script>

<style>
.menu {
  position: absolute;
  top: 50vh;
}
.fixed {
  position: fixed;
  top: 0;
}
</style>
