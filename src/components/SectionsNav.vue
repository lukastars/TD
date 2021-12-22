<template>
  <div class="menu w-full z-10">
    <div class="flex justify-around">
      <button
        v-on:click="setActive('section1')"
        :class="[
          isActive('section1')
            ? 'border-b-4 border-[#044D73] text-[#044D73] py-6 bg-white w-full font-sans font-bold text-lg'
            : 'text-[#585f65] py-6 bg-white w-full font-sans font-bold text-lg',
        ]"
      >
        Section 1
      </button>
      <button
        v-on:click="setActive('section2')"
        :class="[
          isActive('section2')
            ? 'border-b-4 border-[#044D73] text-[#044D73] py-6 bg-white w-full font-sans font-bold text-lg'
            : 'text-[#585f65] py-6 bg-white w-full font-sans font-bold text-lg',
        ]"
      >
        Section 2
      </button>
      <button
        v-on:click="setActive('section3')"
        :class="[
          isActive('section3')
            ? 'border-b-4 border-[#044D73] text-[#044D73] py-6 bg-white w-full font-sans font-bold text-lg'
            : 'text-[#585f65] py-6 bg-white w-full font-sans font-bold text-lg',
        ]"
      >
        Section 3
      </button>
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
    test() {
      console.log('sssss');
    },
  },
};

let num = window.innerHeight / 2;

window.addEventListener('scroll', () => {
  if (window.scrollY > num) {
    document.querySelector('.menu').classList.add('fixed');
  } else {
    document.querySelector('.menu').classList.remove('fixed');
  }
});
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
