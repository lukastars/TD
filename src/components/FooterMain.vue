<template>
  <footer class="px-16 py-4 bg-black text-white flex justify-between">
    <div>
      <p>All rights reserved.Copyright ©{{ year }}</p>
    </div>
    <div class="flex">
      <a href="" class="px-8 underline">Sitemap</a>
      <a href="" class="px-8 underline">Terms and conditions</a>
      <a href="" class="px-8 underline">Privacy</a>
      <a href="" class="pl-8 underline">Help</a>
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
