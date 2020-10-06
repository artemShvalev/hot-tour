<template>
   <div class="formtour">
     <div class="form__title">
       <h3>Заявка на подбор путешествия</h3>
     </div>
     <div class="about">
       <p>НЕМНОГО О ВАС</p>
     </div>
     <div class="first__form">
       <label class="label__name" for="name">Имя<span class="required">*</span></label>
         <input type="text" name="name" id="name">
       <label class="label__tel" for="tel">Телефон</label>
         <input type="tel" name="name" id="tel" placeholder="+7___ ___ __ __">
     </div>
     <div class="about__advice">
        <p>О ПУТЕШЕСТВИИ</p>
     </div>
     <div class="second__form">
       <label for="advice" class="advice">Куда и когда хотите поехать<span class="required">*</span>
       </label>
         <input type="text" name="name" id="advice" placeholder="Континент, страна или город" >
       <label for="when" class="when">Когда</label>
         <input type="date" name="date" id="when" placeholder="Даты или временной  интервал">
     </div>
     <div class="connection">
       <p>Удобный способ связи</p>
     </div>
     <div class="checked">
       <label for="viber" class="label__viber">Viber</label>
       <input type="checkbox" id="viber">

       <label for="whatsapp" class="label__whatsaap">WhatsApp</label>
       <input type="checkbox" id="whatsapp">

       <label for="mail" class="label__mail">Почта</label>
       <input type="checkbox" id="mail">

       <label for="telephone" class="label__telephone">Телефон</label>
       <input type="checkbox" id="telephone">
     </div>
     <div class="about__us">
       <label for="internet">Интернет</label>
       <input type="checkbox" id="internet">

       <label for="recommendation">Рекомендовали друзья</label>
       <input type="checkbox" id="recommendation">

       <label for="soc">Соц.сети</label>
       <input type="checkbox" id="soc">

       <label for="already__went">Уже ездил</label>
       <input type="checkbox" id="already__went">
     </div>
     <div class="rss">
       <input type="checkbox" id="rss"><label for="rss">Получать свежие предложения по электронной
       почте</label>
       <span>Каждую неделю мы делаем для вас обзор лучших экспедиций,
         статей и лайфхаков для путешественников.
         Если вдруг вам не понравится,
         вы сможете отписаться в любой момент.</span>
     </div>
     <div class="personal">
       <input type="checkbox" id="personal"><label for="personal">C обработкой своих персональных
       данных согласен<span class="required">*</span></label>
       <span>Отправляя заявку я подтверждаю согласие с условиями Пользовательского соглашения</span>
     </div>
     <div class="field">
     <p><span class="required">*</span>Поля которые надо обязательно заполнить</p>
     </div>
     <div class="btn">
       <button>Отправить <img src="../assets/img/arrbutton.png" alt=""></button>
     </div>
   </div>
</template>

<script>
export default {
  name: 'FormTour',
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
  .formtour{
    background: #E5E5E5;
    width: 1024px;
    height: 100vh;
    margin: 0 auto;
    background-image: url("../assets/img/ellipse.png");
    background-position: center;
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: center;
    background-size: contain;/*Если что удалить*/
  }
  .form__title{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 43px;
    text-align: center;
    color: #000000;

    position: absolute;
    top: 1575px;
    right:620px;
  }

  .about{
    position: absolute;
    top: 1649px;
    left: 540px;
    padding-top: 70px;

    font-family: Museo Sans Cyrl;
    font-size: 10px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .first__form{
    display: flex;
  }
  .label__name{
    position: absolute;
    top: 1770px;
    padding-left: 100px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  .required{
    color: crimson;
  }
  .label__tel{
    position: absolute;
    top: 1770px;
    padding-left: 500px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  input{
    background: #FFFFFF;
    border: 1px solid #E7E7E7;
    box-sizing: border-box;
    border-radius: 3px;
    width: 380px;
    height: 50px;
  }
  #name{
    position: absolute;
    top: 1785px;
    left:535px;
  }
  #tel{
    position: absolute;
    top: 1785px;
    left:940px;
  }
  .about__advice{
    position: absolute;
    top: 1835px;
    left: 540px;
    padding-top: 70px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .advice{
    position: absolute;
    top: 1940px;
    padding-left: 100px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  #advice{
    position: absolute;
    top: 1955px;
    left:535px;
  }
  .when{
    position: absolute;
    top: 1940px;
    padding-left: 500px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  #when{
    position: absolute;
    top:1955px;
    left:939px;
  }
  .connection{
    position: absolute;
    top: 1970px;
    left: 540px;
    padding-top: 70px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .checked{
    display: flex;
  }
  .label__viber{
    font-family: Museo Sans Cyrl;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2100px;
    left: 555px;
  }
  #viber{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 2120px;
    left: 555px;
  }
  .label__whatsaap{
    font-family: Museo Sans Cyrl;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2100px;
    left: 625px;
  }
  #whatsapp{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 2120px;
    left: 635px;
  }
  .label__mail{
    font-family: Museo Sans Cyrl;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2100px;
    left: 720px;
  }
  #mail{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 2120px;
    left: 720px;
  }
  .label__telephone{
    font-family: Museo Sans Cyrl;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2100px;
    left: 780px;
  }
  #telephone{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 2120px;
    left: 790px;
  }
  .about__us{
    display: flex;
  }

</style>
