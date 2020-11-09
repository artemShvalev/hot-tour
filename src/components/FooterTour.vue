<template>
    <div>
      <div class="footer">
        <div class="img__footer">
        <img id="img" src="../assets/img/footer.png" alt="">
        </div>
        <div class="img__lineup">
        <img src="../assets/img/lineup.png" alt="">
        </div>
        <div class="img__linedown">
        <img src="../assets/img/linedown.png" alt="">
        </div>
      <div class="phones">
        <a href="tel:88001234567">8 (800) 123-45-67</a>
      </div>
      <div class="phones__down">
        <a href="tel:88001234567"><span>8 (800) 123-45-67</span></a>
      </div>
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
    background: #ffffff;
    width: 1024px;
    margin: 0 auto;
    display: flex;
    position: absolute;
    top: 106px;
    left:0;
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
    left: 670px;
    top: 2668px;

    font-family: Museo Sans Cyrl,sans-serif;
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
    top: 2770px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 29px;
    letter-spacing: 0.1em;
    color: #FFFFFF;
  }
  /*mobile*/
  @media (max-width: 375px) {
    .footer{
      position: absolute;
      width: 100%;
      left: -521px;
      top: 754px;
    }
    .img__footer,#img{
      width: 375px;
      position: absolute;
      left: 521px;
    }
    a{
      text-decoration: none;
      color: #ffffff;
      width: 100%;
    }
    span{
      width: 100px;
      height: 100px;
    }
    .phones{
      position: relative;
      left: 611px;
      right: 0;
      bottom: 0;
      font-family: Museo Sans Cyrl, sans-serif;
      font-style: normal;
      font-weight: bold;
      font-size: 24px;
      color: #FFFFFF;
    }
    .phones__down{
      display: flex;
      position: absolute;
      left: 611px;
      top: 2775px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-style: normal;
      font-weight: bold;
      font-size: 24px;
      line-height: 29px;
      letter-spacing: 0.1em;
      color: #FFFFFF;
    }
  }

</style>
