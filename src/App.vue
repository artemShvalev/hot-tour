<template>
  <div id="app">
    <HeaderTour/>
    <MainTour/>
  </div>
</template>

<script>
import HeaderTour from './components/HeaderTour.vue';
import MainTour from './components/MainTour.vue';

export default {
  name: 'App',
  components: { HeaderTour, MainTour },
};
</script>

<style lang="scss">
</style>
