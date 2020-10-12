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
         <input type="text" name="name" id="name"  v-model.trim="name">
       <div class="error__name" v-if="!name">Введите имя</div>
       <label class="label__tel" for="tel">Телефон</label>
         <input type="tel" name="name" id="tel" placeholder="+7___ ___ __ __">
     </div>
     <div class="about__advice">
        <p>О ПУТЕШЕСТВИИ</p>
     </div>
     <div class="second__form">
       <label for="advice" class="advice">Куда и когда хотите поехать<span class="required">*</span>
       </label>
         <input type="text" name="name" id="advice"
                placeholder="Континент, страна или город" v-model.trim="required">
       <div class="error" v-if="!required">Вы длолжны ввести страну или регион</div>
       <label for="when" class="when">Когда</label>
         <input :type="data" name="date" id="when" placeholder="Даты или временной  интервал">
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
     <div class="about__us_text">
       <p>Откуда узнали о нас</p>
     </div>
     <div class="about__us">
       <label for="internet" class="label__internet">Интернет</label>
       <input type="checkbox" id="internet">

       <label for="recommendation" class="label__recommendation">Рекомендовали
         <span class="frends">друзья</span></label>
       <input type="checkbox" id="recommendation">

       <label for="soc" class="label__soc">Соц.сети</label>
       <input type="checkbox" id="soc">

       <label for="already__went" class="label__alredy_went">Уже ездил</label>
       <input type="checkbox" id="already__went">
     </div>
     <div class="rss">
       <input type="checkbox" id="rss"><label for="rss" class="label__rss">
       'Получать свежие предложения по электронной
       почте</label>
       <span class="rss__text">Каждую неделю мы делаем для вас обзор лучших экспедиций,
         статей и лайфхаков для путешественников.
         Если вдруг вам не понравится,
         вы сможете отписаться в любой момент.</span>
     </div>
     <div class="personal">
       <input type="checkbox" id="personal"><label for="personal" class="label__personal">
       C обработкой  персональных
       данных согласен<span class="required">*</span></label>
       <span class="personal__text" >Отправляя заявку я подтверждаю согласие с условиями
         Пользовательского соглашения</span>
     </div>
     <div class="field">
  <p class="field__text"><span class="required">*</span>Поля которые надо обязательно заполнить</p>
     </div>
     <div class="btn">
       <button>Отправить <img id="img" src="../assets/img/arrbutton.png" alt=""></button>
     </div>
   </div>
</template>

<script>
import { required } from 'vuelidate/lib/validators';

export default {
  name: 'FormTour',
  data() {
    return {
      required: '',
      type: '',
      name: '',
    };
  },
  validations: {
    name: required,
  },
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
  .error{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    color: red;
    font-size: 12px;

    position: absolute;
    top: 2019px;
    left:535px;
  }
  .error__name{
    font-family: Museo Sans Cyrl;
    font-style: normal;
    color: red;
    font-size: 12px;

    position: absolute;
    top: 1847px;
    left:535px;
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
    padding: 30px;
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
  .about__us_text{
    position: absolute;
    top: 1970px;
    left: 950px;
    padding-top: 70px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .about__us{
    display: flex;
    padding-left:120px ;
  }
  .label__internet{
    font-family: Museo Sans Cyrl;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2100px;
    left: 950px;
  }
  #internet{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 2120px;
    left: 960px;
  }
  .label__recommendation{
    width: 140px;
    font-family: Museo Sans Cyrl;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2090px;
    left: 1030px;
  }
  .frends{
     padding-left:40px;
  }
  #recommendation{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 2120px;
    left: 1070px;
  }
  .label__soc{
    font-family: Museo Sans Cyrl;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2100px;
    left: 1160px;
  }
  #soc{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 2120px;
    left: 1170px;
  }
  .label__alredy_went{
    font-family: Museo Sans Cyrl;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2100px;
    left: 1260px;
  }
  #already__went{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 2120px;
    left: 1270px;
  }
  /*Rss*/
  .rss{
    display: flex;
  }
  #rss{
    position: absolute;
    width: 15px;
    height: 15px;
    top: 2200px;
    left: 475px;

    background: #FFFFFF;
    border: 1px solid #E7E7E7;
    box-sizing: border-box;
    border-radius: 3px;
  }
  .label__rss{
    position: absolute;
    width: 266px;
    height: 12px;
    top: 2200px;
    left: 500px;

    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: 500;
    font-size: 10px;
    line-height: 12px;
    color: #000000;
  }
  .rss__text{
    position: absolute;
    width: 750px;
    height: 24px;
    left: 500px;
    top: 2238px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    color: #7c7a7a;
  }
  /*personal*/
  .personal{
    display:flex;
  }
  #personal{
    position: absolute;
    width: 15px;
    height: 15px;
    top: 2300px;
    left: 475px;

    background: #FFFFFF;
    border: 1px solid #E7E7E7;
    box-sizing: border-box;
    border-radius: 3px;
  }
  .label__personal{
    position: absolute;
    width: 266px;
    height: 12px;
    top: 2300px;
    left: 500px;

    font-family: Museo Sans Cyrl;
    font-style: normal;
    font-weight: 500;
    font-size: 10px;
    line-height: 12px;
    color: #000000;
  }
  .personal__text{
    position: absolute;
    width: 750px;
    height: 24px;
    left: 500px;
    top: 2338px;

    font-family: Museo Sans Cyrl;
    font-size: 12px;
    line-height: 12px;
    color: #7c7a7a;
  }
  /*field*/
  .field{
    display: flex;
  }
  .field__text{
    position: absolute;
    width: 310px;
    height: 12px;
    left: 500px;
    top: 2390px;

    font-family: Museo Sans Cyrl;
    font-size: 10px;
    line-height: 12px;
  }
  /*btn*/
  .btn{
    position: absolute;
    left: 500px;
    top: 2450px;
  }
  button{
    width: 280px;
    height: 49px;
    background: #FFD241;
    border-radius: 30px;
    font-family: Museo Sans Cyrl;
    font-size: 14px;
    line-height: 14px;
  }
  #img{
   padding-left: 160px;
  }

</style>
