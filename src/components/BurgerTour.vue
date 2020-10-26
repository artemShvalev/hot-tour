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
  button {
    cursor: pointer;
  }

  /* remove blue outline */
  button:focus {
    outline: 0;
  }

  .burger-button {
    position: relative;
    height: 30px;
    width: 32px;
    display: block;
    z-index: 999;
    border: 0;
    border-radius: 0;
    background-color: transparent;
    pointer-events: all;
    transition: transform .6s cubic-bezier(.165,.84,.44,1);
  }

  .burger-bar {
    background-color: #130f40;
    position: absolute;
    top: 50%;
    right: 6px;
    left: 6px;
    height: 2px;
    width: auto;
    margin-top: -1px;
    transition: transform .6s cubic-bezier(.165,.84,.44,1),
    opacity .3s cubic-bezier(.165,.84,.44,1),background-color .6s cubic-bezier(.165,.84,.44,1);
  }

  .burger-bar--1 {
    -webkit-transform: translateY(-6px);
    transform: translateY(-6px);
  }

  .burger-bar--2 {
    transform-origin: 100% 50%;
    transform: scaleX(.8);
  }

  .burger-button:hover .burger-bar--2 {
    transform: scaleX(1);
  }

  .no-touchevents .burger-bar--2:hover {
    transform: scaleX(1);
  }

  .burger-bar--3 {
    transform: translateY(6px);
  }

  #burger.active .burger-button {
    transform: rotate(-180deg);
  }

  #burger.active .burger-bar {
    background-color: #fff;
  }

  #burger.active .burger-bar--1 {
    transform: rotate(45deg)
  }

  #burger.active .burger-bar--2 {
    opacity: 0;
  }

  #burger.active .burger-bar--3 {
    transform: rotate(-45deg)
  }
</style>
