<template>
  <div  class="all">
     <div class="line"></div>
  <div class="formtour"></div>
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
       <label for="when" class="when">Когда?</label>
         <input :type="data" name="date" id="when" placeholder="Даты или временной  интервал">
     </div>
     <div class="connection">
       <p>Удобный способ связи</p>
     </div>
     <div class="chec">
       <label for="viber" class="label__viber">Viber</label>
       <input type="checkbox"
              id="viber" class="input__check"><span class="span__viber"></span>
       <label for="whatsapp" class="label__whatsaap">WhatsApp</label>
       <input type="checkbox" id="whatsapp"><span class="span__w"></span>

       <label for="mail" class="label__mail">Почта</label>
       <input type="checkbox" id="mail"><span class="span__mail"></span>

       <label for="telephone" class="label__telephone">Телефон</label>
       <input type="checkbox" id="telephone"><span class="span__telephone"></span>
     </div>
     <div class="about__us_text">
       <p>Откуда узнали о нас</p>
     </div>
     <div class="about__us">
       <label for="internet" class="label__internet">Интернет</label>
       <input type="checkbox" id="internet"><span class="span__internet"></span>

       <label for="recommendation" class="label__recommendation">Рекомендовали
         <span class="frends">друзья</span></label>
       <input type="checkbox" id="recommendation"><span class="span__recommendation"></span>

       <label for="soc" class="label__soc">Соц.сети</label>
       <input type="checkbox" id="soc"><span class="span__soc"></span>

       <label for="already__went" class="label__alredy_went">Уже ездил</label>
       <input type="checkbox" id="already__went"><span class="span__went"></span>
     </div>
     <div class="rss">
       <input type="checkbox" id="rss"><span class="rss__span"></span>
       <label for="rss" class="label__rss">
       Получать свежие предложения по электронной почте</label>
       <span class="rss__text">Каждую неделю мы делаем для вас обзор лучших экспедиций,
         статей и лайфхаков для путешественников.
         Если вдруг вам не понравится,
         вы сможете отписаться в любой момент.</span>
     </div>
     <div class="personal">
       <input type="checkbox" id="personal"><span class="span__personal" @click="showModal">
       </span><ModalForm v-show="isModalVisible"
                         @close="closeModal"/>
       <label for="personal" class="label__personal">
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
import ModalForm from './_ModalForm.vue';

export default {
  name: 'FormTour',
  data() {
    return {
      required: '',
      type: '',
      name: '',
      span__viber: true,
      hasError: false,
      isModalVisible: false,
    };
  },
  validations: {
    name: required,
  },
  components: {
    ModalForm,
  },
  methods: {
    showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    },
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
    box-sizing: border-box;
  }
  .all{
    margin: 0 auto;
    background-image: url('../assets/img/ellipse.png');
    background-repeat: no-repeat;
    width: 782px;
    height: 570px;
    background-size: contain;
    background-position-y: center;
    background-position-x:200px;
    position: absolute;
    top: 1648px;
    left: 437px;
    z-index: 50000;
  }
  .error{
    font-family: Museo Sans Cyrl,sans-serif;
    font-style: normal;
    color: red;
    font-size: 12px;

    position: absolute;
    top: 500px;
    left:100px;
  }
  .error__name{
    font-family: Museo Sans Cyrl, sans-serif;
    font-style: normal;
    color: red;
    font-size: 12px;

    position: absolute;
    top: 310px;
    left:100px;
  }
  .formtour{
  }
  .form__title{
    font-family: Museo Sans Cyrl, sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 36px;
    line-height: 43px;
    text-align: center;
    color: #000000;

    position: absolute;
    top: 15px;
    left:265px;
  }

  .about{
    position: absolute;
    top: 132px;
    left: 59px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 10px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .first__form{
    display: flex;
  }
  .label__name{
    position: absolute;
    top: 210px;
    left: 100px;

    font-family: Museo Sans Cyrl, sans-serif;
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
    top: 210px;
    left: 520px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  #name{
    background: #FFFFFF;
    border: 1px solid #E7E7E7;
    box-sizing: border-box;
    border-radius: 3px;
    width: 380px;
    height: 50px;
    padding: 30px;
    position: absolute;
    top: 240px;
    left:100px;
  }
  #tel{
    position: absolute;
    top:  240px;
    left: 520px;
    background: #FFFFFF;
    border: 1px solid #E7E7E7;
    box-sizing: border-box;
    border-radius: 3px;
    width: 380px;
    height: 50px;
    padding: 30px;
  }
  .about__advice{
    position: absolute;
    top: 350px;
    left: 59px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 12px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .advice{
    position: absolute;
    top: 400px;
    left: 100px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  #advice{
    position: absolute;
    top: 430px;
    left:100px;
    background: #FFFFFF;
    border: 1px solid #E7E7E7;
    box-sizing: border-box;
    border-radius: 3px;
    width: 380px;
    height: 50px;
    padding: 30px;
  }
  .when{
    position: absolute;
    top: 400px;
    left: 520px;

    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  #when{
    position: absolute;
    top:430px;
    left:520px;
    background: #FFFFFF;
    border: 1px solid #E7E7E7;
    box-sizing: border-box;
    border-radius: 3px;
    width: 380px;
    height: 50px;
    padding: 30px;
  }
  .connection{
    position: absolute;
    top: 500px;
    left: 59px;
    padding-top: 70px;

    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 12px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .check{
    display: flex;
    position: absolute;
  }
  .label__viber{
    display:block;
    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 630px;
    left: 100px;
    width: 40px;
    height: 40px;
  }
  .input__check{
    width: 40px;
    height: 40px;
    border-radius:3px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    position:absolute;
    top: 660px;
    left: 100px;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__viber::before{
    content: "";
    position: relative;
    top: 675px;
    left:110px ;
    display: block;
    width:40px ;
    height: 40px;
    background-size: 19px 11px;
    background: url("../assets/img/checkbox.png") no-repeat;
    opacity: 0;
  }
  .input__check:checked + .span__viber::before{
    opacity: 1;
    transition: all .4s ease-in-out .3s;
  }
  .label__whatsaap{
    display: block;
    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 630px;
    left: 180px;
  }
  #whatsapp{
    width: 40px;
    height: 40px;
    border-radius:3px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    position:absolute;
    top: 660px;
    left: 190px;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__w::before{
    content: "";
    position: relative;
    top: 635px;
    left:200px ;
    display: block;
    width:40px ;
    height: 40px;
    background-size: 19px 11px;
    background: url("../assets/img/checkbox.png") no-repeat;
    opacity: 0;
  }
  #whatsapp:checked + .span__w::before{
    opacity: 1;
    transition: all .4s ease-in-out .3s;
  }
  .label__mail{
    display: block;
    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 630px;
    left: 280px;
  }
  #mail{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 660px;
    left: 280px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__mail::before{
    content: "";
    position: relative;
   top: 595px;
    left:290px ;
    display: block;
    width:40px ;
    height: 40px;
    background-size: 19px 11px;
    background: url("../assets/img/checkbox.png") no-repeat;
    opacity: 0;
  }
  #mail:checked + .span__mail::before{
    opacity: 1;
    transition: all .4s ease-in-out .3s;
  }
  .label__telephone{
    display: block;
    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 630px;
    left: 350px;
  }
  #telephone{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 660px;
    left: 360px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__telephone::before{
    content: "";
    position: absolute;
       top: 675px;
       left: 370px;
    display: block;
    width:40px ;
    height: 40px;
    background-size: 19px 11px;
    background: url("../assets/img/checkbox.png") no-repeat;
    opacity: 0;
  }
  #telephone:checked + .span__telephone::before{
    opacity: 1;
    transition: all .4s ease-in-out .3s;
  }
  .about__us_text{
    position: absolute;
    top: 570px;
    left: 540px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 12px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .about__us{
    display: flex;
    padding-left:120px ;
  }
  .label__internet{
    display: block;
    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 630px;
    left: 540px;
  }
  #internet{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 660px;
    left: 550px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__internet::before{
    content: "";
    position: absolute;
    top: 675px;
    left: 560px;
    display: block;
    width:40px ;
    height: 40px;
    background-size: 19px 11px;
    background: url("../assets/img/checkbox.png") no-repeat;
    opacity: 0;
  }
  #internet:checked + .span__internet::before{
    opacity: 1;
    transition: all .4s ease-in-out .3s;
  }
  .label__recommendation{
    display: block;
    width: 140px;
    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 630px;
    left: 640px;
  }
  .frends{
     padding-left:40px;
  }
  #recommendation{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 660px;
    left: 670px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__recommendation::before{
    content: "";
   position: absolute;
    top: 675px;
    left: 680px;
    display: block;
    width:40px ;
    height: 40px;
    background-size: 19px 11px;
    background: url("../assets/img/checkbox.png") no-repeat;
    opacity: 0;
  }
  #recommendation:checked + .span__recommendation::before{
    opacity: 1;
    transition: all .4s ease-in-out .3s;
  }
  .label__soc{
    display: block;
    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 630px;
    left: 780px;
  }
  #soc{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 660px;
    left: 800px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__soc::before{
    content: "";
   position: absolute;
    top: 675px;
    left: 810px;
    display: block;
    width:40px ;
    height: 40px;
    background-size: 19px 11px;
    background: url("../assets/img/checkbox.png") no-repeat;
    opacity: 0;
  }
  #soc:checked + .span__soc::before{
    opacity: 1;
    transition: all .4s ease-in-out .3s;
  }
  .label__alredy_went{
    display: block;
    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 630px;
    left: 860px;
  }
  #already__went{
    width: 40px;
    height: 40px;
    border-radius:3px;
    position:absolute;
    top: 660px;
    left: 880px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__went::before{
    content: "";
    position: absolute;
    top: 675px;
    left: 890px;
    display: block;
    width:40px ;
    height: 40px;
    background-size: 19px 11px;
    background: url("../assets/img/checkbox.png") no-repeat;
    opacity: 0;
  }
  #already__went:checked + .span__went::before{
    opacity: 1;
    transition: all .4s ease-in-out .3s;
  }
  /*Rss*/
  .rss{
    display: flex;
  }
  #rss{
    position: absolute;
    width: 15px;
    height: 15px;
    top: 748px;
    left: 59px;

    background: #FFFFFF;
    border: 1px solid #E7E7E7;
    box-sizing: border-box;
    border-radius: 3px;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .rss__span::before{
    content: "";
    position: relative;
    top: 628px;
    left: 59px;
    display: block;
    width:15px ;
    height: 15px;
    border-radius: 3px;
    background-size: 4px 9px;
    background: url("../assets/img/checboxSmall.png") no-repeat;
    background-position-y: 4px;
    background-position-x:1px;
    opacity: 0;
  }
  #rss:checked + .rss__span::before{
    opacity: 1;
    transition: all .5s;
  }
  .label__rss{
    display: block;
    position: absolute;
    width: 266px;
    height: 12px;
    top: 750px;
    left: 79px;

    font-family: Museo Sans Cyrl, sans-serif;
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
    top: 780px;
    left: 79px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 12px;
    line-height: 12px;
    color: #C1C1C1;
  }
  /*personal*/
  .personal{
    display:flex;
  }
  #personal{
    position: absolute;
    width: 15px;
    height: 15px;
    top: 870px;
    left: 59px;
    box-sizing: border-box;
    border-radius: 3px;
    border:1px solid #CB0037;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .label__personal{
    display: block;
    position: absolute;
    width: 266px;
    height: 12px;
    top: 870px;
    left: 79px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 10px;
    line-height: 12px;
    color: #000000;
  }
  .span__personal::before{
    content: "";
    position: relative;
    top: 734px;
    left: 58px;
    display: block;
    width:15px ;
    height: 15px;
    border-radius: 3px;
    background-size: 4px 9px;
    background: url("../assets/img/checboxSmall.png") no-repeat;
    background-position-y: 4px;
    background-position-x:1px;
    opacity: 0;
  }
  #personal:checked + .span__personal::before{
    opacity: 1;
    border:1px solid #ac0909;
    transition: all .5s;
    z-index:1 ;
    outline: none;
  }
  .personal__text{
    position: absolute;
    width: 750px;
    height: 24px;
    top: 900px;
    left: 79px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 12px;
    line-height: 12px;
    color: #C1C1C1;
  }
  /*field*/
  .field{
    display: flex;
  }
  .field__text{
    position: absolute;
    width: 310px;
    height: 12px;
    left: 79px;
    top: 970px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 10px;
    line-height: 12px;
  }
  /*btn*/
  .btn{
    position: absolute;
    left: 89px;
    top: 999px;
  }
  button{
    width: 280px;
    height: 49px;
    background: #FFD241;
    border-radius: 30px;
    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 14px;
    line-height: 14px;
    outline: none;
  }
  #img{
   padding-left: 160px;
  }

  @media (max-width: 375px){
    .all{
      background-color: #FFFFFF;
      background-image: none;
    }
    .line{
      position: absolute;
      width: 340px;
      height: 2px;
      left: -420px;
      top: 100px;
      background: #C4C4C4;
    }
    .form__title{
      position: absolute;
      width: 340px;
      height: 87px;
      left: -420px;
      top: 120px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 36px;
      line-height: 43px;
      color: #000000;
    }
    .about{
      position: absolute;
      left: -420px;
      top: 320px;

      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: black;
    }
    .label__name{
      position: absolute;
      left: -400px;
      top: 380px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: black;
    }
    #name{
      position: absolute;
      width: 320px;
      height: 50px;
      left: -410px;
      top: 400px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px
    }
    .error__name{
      font-family: Museo Sans Cyrl, sans-serif;
      font-style: normal;
      color: red;
      font-size: 12px;
      position: absolute;
      left: -400px;
      top: 470px;
      line-height: 12px;
    }
    .label__tel{
      position: absolute;
      width: 49px;
      height: 12px;
      left: -400px;
      top: 500px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: black;
    }
    #tel{
      position: absolute;
      width: 320px;
      height: 50px;
      left: -410px;
      top: 520px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px
    }
    .about__advice{
      position: absolute;
      left: -420px;
      top: 620px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
    }
    .advice{
      position: absolute;
      width: 174px;
      height: 12px;
      left: -400px;
      top: 660px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #advice{
      position: absolute;
      width: 320px;
      height: 50px;
      left: -410px;
      top: 660px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .error{
      font-family: Museo Sans Cyrl,sans-serif;
      font-style: normal;
      color: red;
      font-size: 12px;
      position: absolute;
      left: -400px;
      top: 730px;
      line-height: 12px;
    }
    .when{
      position: absolute;
      width: 38px;
      height: 12px;
      left: -400px;
      top: 770px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
    }
    #when{
      position: absolute;
      width: 320px;
      height: 50px;
      left: -410px;
      top: 790px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    /*Checkboxes*/
    .connection{
      position: absolute;
      left: -410px;
      top: 795px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
    }
    /* Section viber*/
    .label__viber{
      position: absolute;
      left: -400px;
      top: 910px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #viber{
      width: 40px;
      height: 40px;
      border-radius:3px;
      border:1px solid #8C8C8C;
      background-color: #FFFFFF;
      position:absolute;
      top: 940px;
      left: -406px;
      -webkit-appearance: none;
      appearance: none;
      outline: none;
    }
    .span__viber::before{
      content: "";
      position: relative;
      top: 955px;
      left: -396px;
      display: block;
      width:40px ;
      height: 40px;
      background-size: 19px 11px;
      background: url("../assets/img/checkbox.png") no-repeat;
      opacity: 0;
    }
    .input__check:checked + .span__viber::before{
      opacity: 1;
      transition: all .4s ease-in-out .3s;
    }
    /* Section Whatsapp*/
    .label__whatsaap{
      position: absolute;
      top: 910px;
      left: -340px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #whatsapp{
      position: absolute;
      width: 40px;
      height: 40px;
      top: 940px;
      left: -337px;

      background: #FFFFFF;
      border:1px solid #8C8C8C;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .span__w::before{
      content: "";
      position: relative;
      top: 914px;
      left: -327px;
      display: block;
      width:40px ;
      height: 40px;
      background-size: 19px 11px;
      background: url("../assets/img/checkbox.png") no-repeat;
      opacity: 0;
    }
    /* Section mail*/
    .label__mail{
      position: absolute;
      top: 910px;
      left: -250px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #mail{
      position: absolute;
      width: 40px;
      height: 40px;
      top: 940px;
      left: -253px;

      background: #FFFFFF;
      border:1px solid #8C8C8C;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .span__mail::before{
      content: "";
      position: relative;
      top: 875px;
      left: -242px;
      display: block;
      width:40px ;
      height: 40px;
      background-size: 19px 11px;
      background: url("../assets/img/checkbox.png") no-repeat;
      opacity: 0;
    }
    /*Section Telephone*/
    .label__telephone{
      position: absolute;
      top: 910px;
      left: -180px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #telephone{
      position: absolute;
      width: 40px;
      height: 40px;
      top: 940px;
      left: -178px;
      background: #FFFFFF;
      border:1px solid #8C8C8C;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .span__telephone::before{
      content: "";
      position: absolute;
      top: 955px;
      left: -167px;
      display: block;
      width:40px ;
      height: 40px;
      background-size: 19px 11px;
      background: url("../assets/img/checkbox.png") no-repeat;
      opacity: 0;
    }
    /*second section title */
    .about__us_text{
      position: absolute;
      left: -410px;
      top: 1020px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    /*Second section input[type=checkbox] */
    .label__internet{
      position: absolute;
      left: -410px;
      top: 1070px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #internet{
      position: absolute;
      width: 40px;
      height: 40px;
      left: -407px;
      top: 1100px;
      background: #FFFFFF;
      border:1px solid #8C8C8C;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .span__internet::before{
      content: "";
      position: absolute;
      left: -397px;
      top: 1115px;
      display: block;
      width:40px ;
      height: 40px;
      background-size: 19px 11px;
      background: url("../assets/img/checkbox.png") no-repeat;
      opacity: 0;
    }
    /*Рекомендовали друзья*/
    .label__recommendation{
      position: absolute;
      left: -340px;
      top: 1070px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    .frends{
      padding-left:30px;
    }
    #recommendation{
      position: absolute;
      width: 40px;
      height: 40px;
      left: -317px;
      top: 1100px;
      background: #FFFFFF;
      border:1px solid #8C8C8C;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .span__recommendation::before{
      content: "";
      position: absolute;
      left: -308px;
      top: 1115px;
      display: block;
      width:40px ;
      height: 40px;
      background-size: 19px 11px;
      background: url("../assets/img/checkbox.png") no-repeat;
      opacity: 0;
    }
    /*Section Social net*/
    .label__soc{
      position: absolute;
      left: -230px;
      top: 1070px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #soc{
      position: absolute;
      width: 40px;
      height: 40px;
      left: -230px;
      top: 1100px;
      background: #FFFFFF;
      border:1px solid #8C8C8C;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .span__soc::before{
      content: "";
      position: absolute;
      left: -221px;
      top: 1115px;
      display: block;
      width:40px ;
      height: 40px;
      background-size: 19px 11px;
      background: url("../assets/img/checkbox.png") no-repeat;
      opacity: 0;
    }
    /*Section "Already Went"*/
    .label__alredy_went{
      position: absolute;
      left: -162px;
      top: 1070px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #already__went{
      position: absolute;
      width: 40px;
      height: 40px;
      left: -154px;
      top: 1100px;
      background: #FFFFFF;
      border:1px solid #8C8C8C;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .span__went::before{
      content: "";
      position: absolute;
      left: -145px;
      top: 1115px;
      display: block;
      width:40px ;
      height: 40px;
      background-size: 19px 11px;
      background: url("../assets/img/checkbox.png") no-repeat;
      opacity: 0;
    }
    /*rules*/
    .rss{
      display: flex;
    }
    #rss{
      position: absolute;
      width: 15px;
      height: 15px;
      left: -410px;
      top: 1250px;
      background: #FFFFFF;
      border:1px solid #8C8C8C;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .rss__span::before{
      content: "";
      position: relative;
      left: -410px;
      top: 1130px;
      display: block;
      width:15px ;
      height: 15px;
      border-radius: 3px;
      background-size: 4px 9px;
      background: url("../assets/img/checboxSmall.png") no-repeat;
      background-position-y: 4px;
      background-position-x:1px;
      opacity: 0;
    }
    .label__rss{
      position: absolute;
      width: 100%;
      left: -386px;
      top: 1250px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      color: #000000;
    }
    .rss__text{
      position: absolute;
      width: 310px;
      height: 36px;
      left: -386px;
      top: 1265px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 18px;
      color: #C1C1C1;
    }
    /*Personal && Modal window*/
    .personal{
      display:flex;
    }
    #personal{
      position: absolute;
      left: -410px;
      top: 1370px;
      background: #FFFFFF;
      border:1px solid #CB0037;
      box-sizing: border-box;
      border-radius: 3px;
      width:15px ;
      height: 15px;
    }
    .span__personal::before{
      content: "";
      position: absolute;
      left: -410px;
      top: 1370px;
      display: block;
      width:15px ;
      height: 15px;
      border:1px solid #CB0037;
      border-radius: 3px;
      background-size: 4px 9px;
      background: url("../assets/img/checboxSmall.png") no-repeat;
      background-position-y: 4px;
      background-position-x:1px;
      opacity: 0;
    }
    .label__personal{
      position: absolute;
      width: 100%;
      left: -386px;
      top: 1370px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      color: #000000;
    }
    .personal__text{
      position: absolute;
      width: 310px;
      height: 36px;
      left: -386px;
      top: 1390px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 18px;
      color: #C1C1C1;
    }
    /*Field required*/
    .field__text{
      position: absolute;
      width: 310px;
      height: 12px;
      left: -386px;
      top: 1470px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #C1C1C1;
    }
    /*Кнопка*/
    button{
      position: absolute;
      width: 280px;
      height: 49px;
      left: -478px;
      top: 550px;
    }
  }

</style>
