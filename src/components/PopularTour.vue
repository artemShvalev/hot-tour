<template>
  <div>
    <div  class="line"></div>
    <div class="content">
      <div class="popular__title">
        <h2>Популярные туры</h2>
      </div>
      <swiper>
        <swiper-slide>
      <div class="content__box">
        <div class="content__img">
          <img src="../assets/img/popular1.png" alt="">
        </div>
        <div class="box__price">
          <img src="../assets/img/box-price.png" alt="">
          <p class="box__text">37 302 <span>₽</span></p>
        </div>
        <div class="country">
          <p>Турция</p>
        </div>
        <div class="subtitle">
          <h3>Открытие Турции</h3>
        </div>
        <div class="content__img-2">
          <img src="../assets/img/popular2.png" alt="">
        </div>
        <div class="box__price-2">
          <img src="../assets/img/box-price.png" alt="">
          <p class="box__text">145 000 <span>₽</span></p>
        </div>
        <div class="country-2">
          <p>НОРВЕГИЯ, ШПИЦБЕРГЕН</p>
        </div>
        <div class="subtitle-2">
          <h3>От Свальбарда до Груманта</h3>
        </div>
      </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import SwiperCore, { Navigation } from 'swiper';

SwiperCore.use([Navigation]);

export default {
  name: 'PopularTour',
  components: {
    Swiper,
    SwiperSlide,
  },
};
</script>

<style scoped lang="scss">
  @import '~swiper/components/navigation/navigation';
  @font-face {
    font-family: Museo Sans Cyrl;
    src: url('../assets/fonts/Museo Sans Cyrl.ttf') format('opentype');
  }
  * {
    margin: 0;
    padding: 0;
  }

  .swiper-slide{
    width:100%;
  }
  #swiper-slide{
    width:100%;
  }
  .swiper-button-next{
    position: absolute;
    cursor: pointer;
  }
  .content{
    background: #E5E5E5;
    width: 1024px;
    margin: 0 auto;
  }
  .popular__title{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 43px;
    color: #000000;

    position: absolute;
    top: 1077px;
    left: 38%;
    padding-top: 70px;
  }
  .content__box{
    display:flex;
    position: relative;
    top: -340px;
  }
  .content__img{
    padding-left: 100px;
  }
  .box__price{
    position: relative;
    top: 170px;
    left:-380px;
  }
  .box__text{
    font-family: Museo Sans Cyrl;
    font-size: 18px;
    line-height: 22px;
    color: #000000;
    position: relative;
    top:-38px;
    padding-left: 45px;
  }
  .country{
    position: absolute;
    top: 230px;
    padding-left: 100px;

    font-family: Museo Sans Cyrl;
    font-size: 9px;
    line-height: 11px;
    color: #C5B223;
  }
  .subtitle{
    position: absolute;
    padding-left: 100px;
    top: 250px;

    font-family: Museo Sans Cyrl;
    font-size: 18px;
    line-height: 22px;
    color: #000000;
  }
  .content__img-2{
    position: absolute;
    padding-left:500px ;
  }
  .box__price-2{
      position: relative;
      top:167px;
      left: -140px;
  }
  .country-2{
    position: absolute;
    top: 230px;
    padding-left: 500px;

    font-family: Museo Sans Cyrl;
    font-size: 9px;
    line-height: 11px;
    color: #C5B223;
  }
  .subtitle-2{
    position: absolute;
    padding-left: 500px;
    top: 250px;

    font-family: Museo Sans Cyrl;
    font-size: 18px;
    line-height: 22px;
    color: #000000;
  }

  @media (max-width: 576px){
    .content{
      background-color: #FFFFFF;
    }
    .line{
      background-image: url("../assets/img/line.png");
      position: absolute;
      width: 340px;
      height: 2px;
      left: 18px;
      top: 1353px;
    }
    .popular__title{
      position: absolute;
      width: 350px;
      height: 87px;
      left: 70px;
      top: 1346px;

      font-family: Museo Sans Cyrl, sans-serif;
      font-style: normal;
      font-weight: bold;
      font-size: 36px;
      line-height: 43px;
    }
    .content__box{
      position: absolute;
      width: 253px;
      height: 158px;
      top: 1400px;
      left: -95px;
    }
    .subtitle-2{
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 9px;
      line-height: 11px;
      color: #000000;
    }
  }
</style>
