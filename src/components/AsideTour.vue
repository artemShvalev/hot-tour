<template>
<aside>
  <div class="header__aside" @click="closeSidebarPanel"  v-if="isPanelOpen">
    <div class="header__img">
    <img src="../assets/img/close-aside.png" alt="">
    </div>
  </div>
  <div class="forms">
    <div class="country">
    </div>
  </div>
</aside>
</template>

<script>

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
};
</script>

<style scoped lang="scss">
  aside{
    display: flex;
    flex-direction: row;
    justify-content:flex-end;
  }
  .header__aside{
    width: 530px;
    background: #FFD241;
    height: 100vh;
    top: 10px;
    position: absolute;
    right:438px;
    cursor: pointer;
    z-index: 3000;
    opacity: 45%;
  }
  .header__img{
    float:right ;
    padding: 13px 16px
  }

</style>
