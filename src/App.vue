<template>
  <div id="app">
    <HeaderTour/>
    <MainTour/>
    <PopularTour/>
    <FormTour v-model="$data"/>
    <FooterTour/>
  </div>
</template>

<script>
import HeaderTour from './components/HeaderTour.vue';
import MainTour from './components/MainTour.vue';
import PopularTour from './components/PopularTour.vue';
import FormTour from './components/FormTour.vue';
import FooterTour from './components/FooterTour.vue';

export default {
  name: 'App',
  components: {
    HeaderTour,
    MainTour,
    PopularTour,
    FormTour,
    FooterTour,
  },
};
</script>

<style lang="scss" scoped>
  :root {
    box-sizing: border-box;
  }
  *
  ::before,
  ::after {
    box-sizing: inherit;
  }
</style>
