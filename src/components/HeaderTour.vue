<template>
  <div>
    <header class="header">
      <div class="wrapper">
        <div class="burger__header">
          <img class="burger__header" src="../assets/img/burger.png" alt="burger">
        </div>
      </div>
    </header>
</div>
</template>

<script>
export default {
  name: 'MainTour',
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
