<template>
  <div id="app">
    <HeaderTour/>
    <MainTour/>
    <PopularTour/>
    <FormTour/>
  </div>
</template>

<script>
import HeaderTour from './components/HeaderTour.vue';
import MainTour from './components/MainTour.vue';
import PopularTour from './components/PopularTour.vue';
import FormTour from './components/FormTour.vue';

export default {
  name: 'App',
  components: {
    HeaderTour,
    MainTour,
    PopularTour,
    FormTour,
  },
};
</script>

<style lang="scss">
</style>
