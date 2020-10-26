<template>
<aside    v-if="isPanelOpen">
  <div class="header__aside">
    <div class="header__img"  @click="closeSidebarPanel">
    <img src="../assets/img/close-aside.png" alt="" >
    </div>
    <SideInfoTour  v-show="isPanelOpen"/>
  </div>
</aside>
</template>

<script>
import SideInfoTour from './SideInfoTour.vue';

export default {
  name: 'AsideTour',
  data() {
    return {
      isPanelOpen: true,
    };
  },
  methods: {
    closeSidebarPanel() {
      this.isPanelOpen = false;
    },
  },
  props: {
    type: Boolean,
  },
  components: { SideInfoTour },
};
</script>

<style scoped lang="scss">

  .header__aside{
    width: 530px;
    background: #FFD241;
    height: 100vh;
    top: 10px;
    position: absolute;
    right:438px;
    cursor: pointer;
    z-index: 3000;
  }
  .header__img{
    float:right ;
    padding: 10px 10px;
  }
  aside{
    visibility:visible;
  }

</style>
