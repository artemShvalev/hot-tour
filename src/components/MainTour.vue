<template>
  <main>
    <div class="main__title">
      <h1>Горящие туры</h1>
    </div>
    <div  class="line"></div>
    <div class="rectangle">
      <div class="spanish">
        <a href="#"><img class="img__country" src="../assets/img/rectangle.png" alt="">
        <span class="spanish__text">Испания</span></a>
      </div>
      <div class="italia">
        <a href="#"><img class="img__country__italia" src="../assets/img/rectangle2.png" alt="">
        <span class="text__italia">Италия</span></a>
      </div>
      <div class="iceland">
       <a href="#"><img class="img__country__iceland" src="../assets/img/rectangle2.png" alt="">
        <span class="text__iceland">Исландия</span></a>
      </div>
      <div class="turkey">
        <a href="#"><img class="img__country__turkey" src="../assets/img/rectangle2.png" alt="">
        <span class="text__turkey">Турция</span></a>
      </div>
    </div>
  </main>
</template>

<script>

export default {
  name: 'MainTour',
};
</script>

<style scoped lang="scss">
  @import '~swiper/swiper';
  @font-face {
    font-family: Museo Sans Cyrl;
    src: url('../assets/fonts/Museo Sans Cyrl.ttf') format('opentype');
  }
  * {
    margin: 0;
    padding: 0;
  }
  #swiper-slide{
    width:100%;
  }
  .swiper-button-next{
    position: absolute;
    cursor: pointer;
    right:70px;
    top: -120px;
  }

  main{
    background: #ffffff;
    width: 1024px;
    margin: 0 auto;
  }
  .main__title{
    text-align: center;
    padding-top:35px;
    font-family: Museo Sans Cyrl, sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 43px;
    color: #000000;
  }
  .rectangle,a{
    display:flex;
    margin: 0;
    padding-top: 45px;
    position:relative;
    right:220px;
    top: -106px;
  }
  .spanish:hover{
    background-image: url("../assets/img/rec-1.png");
    background-repeat: no-repeat;
    width: 100px;
    height: 32px;
    position: absolute;
    background-position-x: 530px;
  }
  .spanish__text:after{
    color: #FFFFFF;
  }

  .img__country{
    position: absolute;
    left: 540px;
    top: 200px;
  }
  .img__country__italia{
    position: absolute;
    left: 640px;
    top: 200px;
  }
  .img__country__iceland{
    position: absolute;
    left: 740px;
    top: 200px;
  }
  .img__country__turkey{
    position: absolute;
    left: 840px;
    top: 200px;
  }
  .spanish__text{
    font-family: Museo Sans Cyrl,sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 17px;
    color: #000000;

    position: absolute;
    top: 207px;
    left: 552px;
  }
  .text__italia{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 17px;
    color: #000000;

    position: absolute;
    top: 207px;
    left: 670px;
  }
  .text__iceland{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 17px;
    color: #000000;

    position: absolute;
    top: 207px;
    left: 760px;
  }
  .text__turkey{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 17px;
    color: #000000;

    position: absolute;
    top: 207px;
    left: 860px;
  }
  .img__1{
    width:380px;
  }
  .block-1{
    display: flex;
    flex-direction: column;
    padding-left:100px ;
    position: absolute;
  }
  .box__price{
    position: relative;
    top: -53px;
  }
  .block__2{
    display: flex;
    flex-direction: column;
    padding-left:500px ;
  }
  .box__price-2{
    position: relative;
    top: -53px;
  }
  .block__3{
    display: flex;
    flex-direction: column;
    padding-left:100px ;
  }
  .box__price-3{
    position: relative;
    top: -53px;
  }
  .block-4{
    display: flex;
    flex-direction: column;
    padding-left:500px;
    position: relative;
    top: -430px;
  }
  .this__price{
    font-family: Museo Sans Cyrl;
    font-size: 18px;
    line-height: 22px;
    color: #000000;
    position: relative;
    top: -63px;
    padding: 25px 14px;
  }
  .country{
    font-family: Museo Sans Cyrl;
    font-size: 9px;
    line-height: 11px;
    color: #C5B223;
    position: relative;
    top: -118px;
  }
  .subtitle{
    font-family: Museo Sans Cyrl;
    font-size: 18px;
    line-height: 22px;
    color: #000000;
    position: relative;
    top:-113px;
  }
  .tags{
    font-family: Museo Sans Cyrl;
    font-size: 9px;
    line-height: 13px;
    color: #8C8C8C;
    width: 340px;
    position: relative;
    top:-97px;
  }
  .date{
    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 11px;
    color: #000000;
    width: 340px;
    position: relative;
    top:-87px;
    z-index:5;
  }
  .avia__enabled{
    width: 340px;
    position: relative;
    top:-67px;
  }
  .avia__text{
    font-family: Museo Sans Cyrl;
    font-size: 9px;
    line-height: 11px;
    color:#FFFFFF;
    position: relative;
    top:-17px;
    padding-left:12px;
    padding-bottom:10px ;
  }
  .this__price-4{
    font-family: Museo Sans Cyrl;
    font-size: 18px;
    line-height: 22px;
    color: #000000;
    position: relative;
    top: -63px;
    padding: 25px 14px;
  }
  .country__4{
    font-family: Museo Sans Cyrl;
    font-size: 9px;
    line-height: 11px;
    color: #C5B223;
    position: relative;
    top: -118px;
  }
  .subtitle__4{
    font-family: Museo Sans Cyrl;
    font-size: 18px;
    line-height: 22px;
    color: #000000;
    position: relative;
    top:-113px;
  }
  .date__4{
    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 11px;
    color: #000000;
    width: 340px;
    position: relative;
    top:-87px;
  }
  .tour{
    width: 340px;
    position: relative;
    top:-67px;
  }
  .tour__text{
    font-family: Museo Sans Cyrl;
    font-size: 9px;
    line-height: 11px;
    color:#FFFFFF;
    position: relative;
    top:-17px;
    padding-left:12px;
    padding-bottom:10px ;
  }
  @media (max-width: 576px) {
    main{
      width: 375px;
      background: #FFFFFF;
    }
    .line{
      background: url("../assets/img/line.png");
      width: 340px;
      height: 2px;
      background: #C4C4C4;
      margin-left: 15px;
      margin-top: 40px;
    }
    .main__title{
      text-align: center;
      padding-top:35px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-style: normal;
      font-weight: bold;
      font-size: 26px;
      line-height: 43px;
      color: #000000;
      padding-right: 10px;
      padding-left: 10px;
    }
    .rectangle{
      display: none;
    }
  }
</style>
