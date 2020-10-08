<template>
    <div>
      <div class="footer">
        <div class="img__footer">
        <img src="../assets/img/footer.png" alt="">
        </div>
        <div class="img__lineup">
        <img src="../assets/img/lineup.png" alt="">
        </div>
        <div class="img__linedown">
        <img src="../assets/img/linedown.png" alt="">
        </div>
      </div>
      <div class="phones">
        <span>8 (800) 123-45-67</span>
      </div>
      <div class="phones__down">
        <span>8 (800) 123-45-67</span>
      </div>
    </div>
</template>

<script>
export default {
  name: 'FooterTour',
};
</script>

<style scoped lang="scss">
  @font-face {
    font-family: Museo Sans Cyrl;
    src: url('../assets/fonts/Museo Sans Cyrl.ttf') format('opentype');
  }
  * {
    margin: 0;
    padding: 0;
  }
  .footer{
    background: #E5E5E5;
    width: 1024px;
    margin: 0 auto;
    display: flex;
    position: absolute;
    top: -106px;
    left:0px;
  }
  .img__footer{
    position: absolute;
    width: 941px;
    height: 197px;
    left: 523px;
    top: 2630px;
    background: #272727;
  }
  .img__lineup{
    position: absolute;
    width: 941px;
    height: 197px;
    left: 521px;
    top: 2629px;
  }
  .img__linedown{
    position: absolute;
    width: 941px;
    top: 2755px;
    left: 523px;
  }
  .phones{
    position: absolute;
    width: 246px;
    height: 29px;
    left: 670px;
    top: 2551px;

    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 29px;
    letter-spacing: 0.1em;
    color: #FFFFFF;
  }
  .phones__down{
    position: absolute;
    width: 246px;
    height: 29px;
    left: 670px;
    top: 2679px;

    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 29px;
    letter-spacing: 0.1em;
    color: #FFFFFF;
  }

</style>
