<template>
  <div id="app">
    <NavHeader v-bind:isEnglish="isEnglish" v-on:switch-to-english="switchToEng"/>
    <HomeMain v-bind:isEnglish="isEnglish"/>
    <HomeFooter v-bind:isEnglish="isEnglish"/>
  </div>
</template>

<script>
import NavHeader from './components/NavHeader.vue';
import HomeMain from './components/HomeMain.vue';
import HomeFooter from './components/HomeFooter.vue';

export default {
  name: 'App',
  components: {
    NavHeader,
    HomeMain,
    HomeFooter
  },
  data() {
    return {
      isEnglish: true
    }
  },
  methods: {
    switchToEng(boolValue) {
      this.isEnglish = (boolValue == 'true');
    }
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
}
</style>
