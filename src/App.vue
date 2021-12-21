<template>
  <HeroSection />
  <SectionsNav />
  <SectionOne />
  <SectionTwo />
</template>

<script>
import HeroSection from './components/HeroSection.vue';
import SectionsNav from './components/SectionsNav.vue';
import SectionOne from './components/SectionOne.vue';
import SectionTwo from './components/SectionTwo.vue';

import './assets/main.css';

export default {
  name: 'App',
  components: {
    HeroSection,
    SectionsNav,
    SectionOne,
    SectionTwo,
  },
};
</script>

<style>
body {
  background-color: #f8f8f8;
}
</style>
