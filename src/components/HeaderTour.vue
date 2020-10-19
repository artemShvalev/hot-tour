<template>
  <div>
    <header class="header">
      <div class="wrapper">
        <div class="burger__header" @click="open">
          <img class="burger__header" src="../assets/img/burger.png" alt="burger">
          <AsideTour v-show="showAside"/>
        </div>
      </div>
    </header>
</div>
</template>

<script>
import AsideTour from './AsideTour.vue';

export default {
  name: 'HeaderTour',
  data() {
    return {
      showAside: false,
    };
  },
  components: { AsideTour },
  methods: {
    open() {
      this.showAside = true;
    },
  },
};
</script>

<style scoped lang="scss">
  *{
    margin: 0 auto;
  }
  .header{
    height: 70px;
    width: 1024px;
    background: #FFD241;
  }
  .burger__header{
   float:right;
    padding: 10px;
  }
</style>
