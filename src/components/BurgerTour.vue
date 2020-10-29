<template>
  <div>
    <header class="header" >
      <div class="wrapper">
        <div class="burger__header"  @click="open">
          <img
            :class="{'active': isBurgerActive}" src="../assets/img/burger.png" alt="burger">
        </div>
      </div>
      <SideTour v-if="isBurgerActive"/>
    </header>
</div>
</template>

<script>
import SideTour from './SideTour.vue';

export default {
  name: 'HeaderTour',
  data() {
    return {
      isBurgerActive: false,
    };
  },
  methods: {
    open() {
      this.isBurgerActive = !this.isBurgerActive;
    },
  },
  components: { SideTour },
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
    padding: 12px;
    cursor: pointer;
  }
  .active{
    cursor: pointer;
  }
  .hidden {
    visibility: hidden;
  }
  // Small devices (landscape phones, 576px and up)
  @media (max-width:375px ) {
    html,body{
      margin: 0;
    }
    .header{
       width:375px;
       height: 70px;
       margin:0 auto;
    }
    .burger__header{
      float:right;
      padding: 25px;
      cursor: pointer;
    }
  }
</style>
