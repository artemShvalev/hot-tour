<template>
  <div class="main__image block-1">
    <swiper
      id="swiper-slide">
      <swiper-slide >
        <img class="img__1" src="../assets/img/1.png" alt="italic">
    <div class="box__price">
      <img src="../assets/img/box-price.png" alt="">
      <p class="this__price">от 118 112 <span class="r">₽</span></p>
    </div>
    <div class="country">
      <p>Италия</p>
    </div>
    <div class="subtitle">
      <h3>Под небом тосканы</h3>
    </div>
    <div class="tags">
      <p>Сансеполькро — (Перуджа) — Ассизи — Губбио — (Сиена) —
        Ла Верна — Ангиари — Монтерки —
        Ареццо — Кортона — (Пиенца) - (Монтепульчано)</p>
    </div>
    <div class="date">
      <p>8 дней / 7 ночей Русский язык<br>
        27.04.19 - 04.05.19и еще 15 дат</p>
    </div>
    <div class="avia__enabled">
      <img src="../assets/img/red-box.png" alt="">
      <p class="avia__text">Авиаперелет включен!</p>
    </div>
      </swiper-slide>
    </swiper>
  </div>
  <div class="block__2">
    <swiper
      class="swiper-slide">
      <swiper-slide >
    <div class="block__img-2">
      <div>
        <img src="../assets/img/2.png" alt="island">
      </div>
      <div class="box__price-2">
        <img src="../assets/img/box-price.png" alt="">
        <p class="this__price"> 140 715 <span>₽</span></p>
      </div>
      <div class="country">
        <p>Исландия</p>
      </div>
      <div class="subtitle">
        <h3>Майские каникулы в Исландии</h3>
      </div>
      <div class="tags">
        <p>Рейкьявик — Тингвеллир — Гюдльфосс — Скафтафедль —
          Сельяландсфосс — Скоугафосс — Йёкюльсаурлоун — Голубая Лагуна —
          Снайфельсйёкутль — Arnarstapi — Рейкьявик</p>
      </div>
      <div class="date">
        <p>8 дней / 7 ночей Русский язык<br>
          27.04.19 - 04.05.19</p>
      </div>
    </div>
      </swiper-slide>
  </swiper>
  </div>
  <div class="block__3">
    <swiper
      class="swiper-slide">
      <swiper-slide >
    <div class="block__img-3">
      <div>
        <img src="../assets/img/3.png" alt="island">
      </div>
      <div class="box__price-3">
        <img src="../assets/img/box-price.png" alt="">
        <p class="this__price">37 302  <span>₽</span></p>
      </div>
      <div class="country">
        <p>Турция</p>
      </div>
      <div class="subtitle">
        <h3>Открытие Турции</h3>
      </div>
      <div class="tags">
        <p>Стамбул — Анкара — Каппадокия —
          Конья — Памуккале — Эфес — Кушадасы —
          Пергам — Ассос — Троя — Стамбул</p>
      </div>
      <div class="date">
        <p>8 дней / 7 ночей Русский язык<br>
          28.04.19 - 05.05.19и еще 3 даты</p>
      </div>
    </div>
      </swiper-slide>
    </swiper>
  </div>
  <div class="block-4">
    <swiper
      class="swiper-slide">
      <swiper-slide >
    <div>
      <img src="../assets/img/4.png" alt="italic">
    </div>
    <div class="box__price">
      <img src="../assets/img/box-price.png" alt="">
      <p  class="this__price-4">145 000 <span>₽</span></p>
    </div>
    <div class="country__4">
      <p>НОРВЕГИЯ, ШПИЦБЕРГЕН</p>
    </div>
    <div class="subtitle__4">
      <h3>От Свальбарда до Груманта</h3>
    </div>
    <div class="date__4">
      <p>8 дней / 7 ночей Русский язык <br>
        27.04.19 - 04.05.19 и еще 15 дат</p>
    </div>
    <div class="tour">
      <img src="../assets/img/red-box.png" alt="">
      <p class="tour__text">Гарантированный тур!</p>
    </div>
      </swiper-slide>
    </swiper>
  </div>
  <div class="swiper-button-next" @click="onSlideChange">
    <img src="../assets/img/arr-next.png" alt="">
  </div>
  <MainTourSlider v-if="onSlideChange(+1)"/>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import MainTourSlider from './MainTourSlider.vue';

export default {
  name: 'SliderTour',
  components: {
    Swiper,
    SwiperSlide,
    MainTourSlider,
  },
  methods: {
    onSwiper(swiper) {
      console.log(swiper);
    },
    onSlideChange() {
      this.$emit(this.onSlideChange(+1));
    },
  },
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
  .swiper-slide{
    width:100%;
  }
  #swiper-slide{
    width:100%;
  }
  .swiper-button-next{
    position: absolute;
    left: 72%;
    top: 58%;
    cursor: pointer;
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

</style>
