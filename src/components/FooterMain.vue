<template>
  <footer
    class="px-9 text-xs sm:text-md sm:px-16 py-4 bg-black text-white flex flex-col sm:flex-row justify-between"
  >
    <div class="flex justify-center pb-5 sm:pb-0">
      <p>All rights reserved.Copyright ©{{ year }}</p>
    </div>
    <div class="flex">
      <a href="" class="px-5 lg:px-8 underline">Sitemap</a>
      <a href="" class="px-5 lg:px-8 underline">Terms and conditions</a>
      <a href="" class="px-5 lg:px-8 underline">Privacy</a>
      <a href="" class="px-5 lg:pl-8 underline">Help</a>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterMain',
  data() {
    return {
      year: 0,
    };
  },
  methods: {
    getYear() {
      const d = new Date();
      let year = d.getFullYear();
      this.year = year;
    },
  },
  mounted() {
    this.getYear();
  },
};
</script>

<style></style>
