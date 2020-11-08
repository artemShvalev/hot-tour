<template>
  <div class="line"></div>
  <div class="content">
    <div class="popular__title">
      <h2>Популярные туры</h2>
    </div>
    <swiper
      navigation
      :speed="700"
      :watchOverflow="true"
      :centeredSlidesBounds="true"
      :followFinger="true"
      :resistanceRatio="0.9"
      :watchSlidesProgress="true"
      autoplay
    >
      <swiper-slide>
        <div class="content__box">
          <div class="content__img">
            <img src="../assets/img/popular1.png" alt="" />
          </div>
          <div class="box__price">
            <img src="../assets/img/box-price.png" alt="" />
            <p class="box__text">37 302 <span>₽</span></p>
          </div>
          <div class="country">
            <p>Турция</p>
          </div>
          <div class="subtitle">
            <h3>Открытие Турции</h3>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="content__img-2 slider2__img">
          <img src="../assets/img/popular2.png" alt="" />
        </div>
        <div class="box__price-2">
          <img src="../assets/img/box-price.png" alt="" />
          <p class="box__text">145 000 <span>₽</span></p>
        </div>
        <div class="country-2">
          <p>НОРВЕГИЯ, ШПИЦБЕРГЕН</p>
        </div>
        <div class="subtitle-2">
          <h3>От Свальбарда до Груманта</h3>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="content__box slider__3-box">
          <div class="content__img slider__content-img">
            <img src="../assets/img/popular1.png" alt="" />
          </div>
          <div class="box__price slider__3box-price">
            <img src="../assets/img/box-price.png" alt="" />
            <p class="box__text">37 302 <span>₽</span></p>
          </div>
          <div class="country slider__3-counter">
            <p>Турция</p>
          </div>
          <div class="subtitle slider__3-subtitle">
            <h3>Открытие Турции</h3>
          </div>
          <div class="content__img-2  slider3__iceland">
            <img src="../assets/img/popular2.png" alt="" />
          </div>
          <div class="box__price-2 slider3__iceland">
            <img src="../assets/img/box-price.png" alt="" />
            <p class="box__text">145 000 <span>₽</span></p>
          </div>
          <div class="country-2 slide3__iceland">
            <p>НОРВЕГИЯ, ШПИЦБЕРГЕН</p>
          </div>
          <div class="subtitle-2  slide3__iceland-salvabard">
            <h3>От Свальбарда до Груманта</h3>
          </div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="content__box slider__3-box slider4__mobile">
          <div class="content__img slider__content-img slider4__img">
            <img src="../assets/img/popular1.png" alt="" />
          </div>
          <div class="box__price slider__3box-price slider4__box-price">
            <img src="../assets/img/box-price.png" alt="" />
            <p class="box__text">37 302 <span>₽</span></p>
          </div>
          <div class="country slider__3-counter slider4__country">
            <p>Турция</p>
          </div>
          <div class="subtitle slider__3-subtitle slider4__subtitle">
            <h3>Открытие Турции</h3>
          </div>
          <div class="content__img-2  slider4__content">
            <img src="../assets/img/popular2.png" alt="" />
          </div>
          <div class="box__price-2  slider4__price">
            <img src="../assets/img/box-price.png" alt="" />
            <p class="box__text">145 000 <span>₽</span></p>
          </div>
          <div class="country-2 slider4__norwegy">
            <p>НОРВЕГИЯ, ШПИЦБЕРГЕН</p>
          </div>
          <div class="subtitle-2 slider4__svalbarta">
            <h3>От Свальбарда до Груманта</h3>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import SwiperCore, { Navigation } from 'swiper';

import 'swiper/swiper.scss';
import 'swiper/components/navigation/navigation.scss';

SwiperCore.use([Navigation]);

export default {
  name: 'PopularTour',
  data() {
    return {
      init: true,
      setWrapperSize: true,
      autoplay: {
        delay: 5000,
      },
    };
  },
  components: {
    Swiper,
    SwiperSlide,
  },
};
</script>

<style scoped lang="scss">
@font-face {
  font-family: Museo Sans Cyrl;
  src: url("../assets/fonts/Museo Sans Cyrl.ttf") format("opentype");
}
* {
  margin: 0;
  padding: 0;
}
.swiper-container {
  margin: 0;
  padding: 0;
  display: flex;
  height: auto;
  width: 100%;
}
.swiper-slide {
  margin-right: 0;
}
.content {
  background: #ffffff;
  width: 1024px;
  margin: 0 auto;
  position: absolute;
  top: 1000px;
  left: 440px;
}
.popular__title {
  font-family: Museo Sans Cyrl, sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 43px;
  color: #000000;

  position: absolute;
  left: 38%;
  padding-top: 70px;
}
.content__box {
  height: 500px;
  display: inline-block;
}
.content__img {
  position: absolute;
  top: 200px;
  padding-left: 30px;
}
.box__price {
  position: absolute;
  top: 370px;
  left: 30px;
}
.box__text {
  font-family: Museo Sans Cyrl, sans-serif;
  font-size: 18px;
  line-height: 22px;
  color: #000000;
  position: relative;
  top: -38px;
  padding-left: 45px;
}
.country {
  position: absolute;
  top: 430px;
  padding-left: 30px;

  font-family: Museo Sans Cyrl, sans-serif;
  font-size: 9px;
  line-height: 11px;
  color: #c5b223;
}
.subtitle {
  position: absolute;
  padding-left: 30px;
  top: 450px;

  font-family: Museo Sans Cyrl, sans-serif;
  font-size: 18px;
  line-height: 22px;
  color: #000000;
}
.content__img-2 {
  position: absolute;
  top: 202px;
  left: -530px;
}
.box__price-2 {
  position: absolute;
  left: -530px;
  top: 370px;
}
.country-2 {
  position: absolute;
  top: 430px;
  left: -530px;

  font-family: Museo Sans Cyrl, sans-serif;
  font-size: 9px;
  line-height: 11px;
  color: #c5b223;
}
.subtitle-2 {
  position: absolute;
  top: 450px;
  left: -530px;

  font-family: Museo Sans Cyrl;
  font-size: 18px;
  line-height: 22px;
  color: #000000;
}
.slider__3-box {
  height: 500px;
  display: inline-block;
}
.slider__content-img {
  position: absolute;
  left: -1000px;
}
.slider__3box-price {
  position: absolute;
  left: -970px;
}
.slider__3-counter {
  position: absolute;
  left: -999px;
}
.slider__3-subtitle {
  position: absolute;
  left: -999px;
}
.swiper-slide-active:nth-last-child(4) {
  display: none;
}
/*mobile*/
@media (max-width: 375px) {
  .swiper-container {
    position: absolute;
    top: 100px;
    left: -420px;
    max-width: 800px;
  }
  .swiper-wrapper{
  }
  .swiper-slide-next{
  }
  .swiper-slide {
  }
  /*1 слайд */
  .content__img {
    width: 253px;
    height: 158px;
    position: absolute;
    left: 100px;
  }
  .slider__content-img {
    z-index: 1;
    width: 253px;
    height: 158px;
  }
  .content__box {
    position: relative;
    left: 0;
    padding: 30px;
  }
  .box__price {
  }
  /*2 слайд*/
  .slider2__img{
    z-index: 5;
    width: 253px;
    height: 158px;
    position: absolute;
    left: 245px;
  }
  /*3 слайд */
  .slider__3-box {
    z-index: 5;
    width: 253px;
  }
  .slider__3box-price{
  }
  .slider__3-counter{
  }
  .slider__3-subtitle{
  }
  .slider3__iceland{
    z-index: 5;
    width: 253px;
  }
  .slider3__iceland{
  }
  .slide3__iceland{
  }
  .slide3__iceland-salvabard{
  }
  /*4 слайд*/
  .slider4__mobile {
    z-index: 5;
    width: 253px;
    position: absolute;
  }
  .slider4__img{
        z-index: 5;
    width: 253px;
    position: absolute;
  }
  .slider4__box-price{
  }
  .slider4__country{
  }
  .slider4__subtitle{
  }

  .slider__content-img {
    width: 200px;
    position: relative;
    right: 600px;
  }
  .slider__3box-price {
  }
  .line {
    background-image: url("../assets/img/line.png");
    position: absolute;
    width: 340px;
    height: 2px;
    left: 18px;
    top: 1100px;
  }
  .popular__title {
    position: absolute;
    width: 300px;
    left: -400px;
    top: 100px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 43px;
  }
  .content__box {
  }
  .subtitle-2 {
  }
  .content__img-2 {
  }
}
</style>
