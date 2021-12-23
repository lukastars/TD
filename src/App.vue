<template>
  <HeroSection />
  <SectionsNav />
  <SectionOne />
  <SectionTwo />
  <SectionThree />
  <FooterMain />
</template>

<script>
import HeroSection from './components/HeroSection.vue';
import SectionsNav from './components/SectionsNav.vue';
import SectionOne from './components/SectionOne.vue';
import SectionTwo from './components/SectionTwo.vue';
import SectionThree from './components/SectionThree.vue';
import FooterMain from './components/FooterMain.vue';

import './assets/main.css';

export default {
  name: 'App',
  components: {
    HeroSection,
    SectionsNav,
    SectionOne,
    SectionTwo,
    SectionThree,
    FooterMain,
  },
};
</script>

<style>
body {
  background-color: #f8f8f8;
}
</style>
