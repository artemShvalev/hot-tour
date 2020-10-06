<template>
  <main>
    <div class="main__title">
      <h1>Горящие туры</h1>
    </div>
    <div class="rectangle">
      <div class="spanish">
        <a href="#"><img class="img__country" src="../assets/img/rectangle.png" alt=""></a>
        <span class="spanish__text">Испания</span>
      </div>
      <div class="italia">
        <a href="#"><img class="img__country__italia" src="../assets/img/rectangle2.png" alt=""></a>
        <span class="text__italia">Италия</span>
      </div>
      <div class="iceland">
       <a href="#"><img class="img__country__iceland" src="../assets/img/rectangle2.png" alt=""></a>
        <span class="text__iceland">Исландия</span>
      </div>
      <div class="turkey">
        <a href="#"><img class="img__country__turkey" src="../assets/img/rectangle2.png" alt=""></a>
        <span class="text__turkey">Турция</span>
      </div>
    </div>
    <div class="main__image block-1">
      <div>
        <img src="../assets/img/1.png" alt="italic">
      </div>
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
    </div>
    <div class="block__2">
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
    </div>
    <div class="block__3">
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
    </div>
    <div class="block-4">
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
    </div>
  </main>
</template>

<script>
export default {
  name: 'MainTour',
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

  main{
    background: #E5E5E5;
    width: 1024px;
    margin: 0 auto;
  }
  .main__title{
    text-align: center;
    padding-top:45px;
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 43px;
    color: #000000;
  }
  .rectangle,a{
    display:flex;
    margin: 0px;
    padding-top: 30px;
  }

  .img__country{
    margin: 0px;
    padding-left: 100px;
  }
  .img__country__italia{
    padding-left:5px ;
  }
  .img__country__iceland{
    padding-left:5px ;
  }
  .spanish__text{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 17px;
    color: #000000;

    position: absolute;
    top:234px;
    left:30% ;
  }
  .text__italia{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 17px;
    color: #000000;

    position: relative;
    top: -25px;
    left: 40%;
  }
  .text__iceland{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 17px;
    color: #000000;

    position: relative;
    top: -25px;
    left: 23%;
  }
  .text__turkey{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 17px;
    color: #000000;

    position: relative;
    top: -25px;
    left: 23%;
    left: 23%;
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
