<template>
   <div class="formtour">
     <div class="line"></div>
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
    width: 1024px;
    height: 100vh;
    margin: 0 auto;
    background: #E5E5E5 url("../assets/img/ellipse.png") no-repeat center;
    background-position-x: center;
    background-position-y: center;
    background-size: contain;/*Если что удалить*/
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
    top: 1575px;
    right:620px;
  }

  .about{
    position: absolute;
    top: 1649px;
    left: 540px;
    padding-top: 70px;

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
    top: 1770px;
    padding-left: 100px;

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
    top: 1770px;
    padding-left: 500px;

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
    top: 1835px;
    left: 540px;
    padding-top: 70px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 12px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .advice{
    position: absolute;
    top: 1940px;
    padding-left: 100px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  #advice{
    position: absolute;
    top: 1955px;
    left:535px;
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
    top: 1940px;
    padding-left: 500px;

    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 12px;
    line-height: 12px;
    text-align: center;
    color: #000000;
  }
  #when{
    position: absolute;
    top:1955px;
    left:939px;
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
    top: 1970px;
    left: 540px;
    padding-top: 70px;

    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 12px;
    line-height: 12px;
    border-bottom:2px solid #000000;
  }
  .check{
    display: flex;
    position: relative;
  }
  .label__viber{
    display:block;
    font-family: Museo Sans Cyrl,sans-serif;
    font-size: 16px;
    line-height: 12px;
    position: absolute;
    top: 2100px;
    left: 555px;
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
    top: 2120px;
    left: 555px;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__viber::before{
    content: "";
    position: relative;
    top: 350px;
    left: 125px;
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
    top: 2100px;
    left: 625px;
  }
  #whatsapp{
    width: 40px;
    height: 40px;
    border-radius:3px;
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    position:absolute;
    top: 2120px;
    left: 635px;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__w::before{
    content: "";
    position: relative;
    top: 310px;
    left: 205px;
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
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__mail::before{
    content: "";
    position: relative;
    top: 270px;
    left: 290px;
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
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__telephone::before{
    content: "";
    position: relative;
    top: 230px;
    left: 360px;
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
    top: 1970px;
    left: 950px;
    padding-top: 70px;

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
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__internet::before{
    content: "";
    position: relative;
    top: 188px;
    left: 410px;
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
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__recommendation::before{
    content: "";
    position: relative;
    top: 188px;
    left: 480px;
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
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__soc::before{
    content: "";
    position: relative;
    top: 188px;
    left: 540px;
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
    border:1px solid #8C8C8C;
    background-color: #FFFFFF;
    -webkit-appearance: none;
    appearance: none;
    outline: none;
  }
  .span__went::before{
    content: "";
    position: relative;
    top: 188px;
    left: 601px;
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
    top: 2200px;
    left: 475px;

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
    top: 217px;
    left: 36px;
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
    top: 2200px;
    left: 500px;

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
    left: 500px;
    top: 2238px;

    font-family: Museo Sans Cyrl, sans-serif;
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
    top: 2300px;
    left: 500px;

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
    top: 300px;
    left: 34px;
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
    border:1px solid #FFFFFF;
    transition: all .5s;
    z-index:1 ;
    outline: none;
  }
  .personal__text{
    position: absolute;
    width: 750px;
    height: 24px;
    left: 500px;
    top: 2338px;

    font-family: Museo Sans Cyrl, sans-serif;
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

    font-family: Museo Sans Cyrl, sans-serif;
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
    font-family: Museo Sans Cyrl, sans-serif;
    font-size: 14px;
    line-height: 14px;
  }
  #img{
   padding-left: 160px;
  }

  @media (max-width: 576px){
    .formtour{
      background-color: #FFFFFF;
      background-image: none;
    }
    .line{
      position: absolute;
      width: 340px;
      height: 2px;
      left: 52px;
      top: 1954px;
      background: #C4C4C4;
    }
    .form__title{
      position: absolute;
      width: 340px;
      height: 87px;
      left: 18px;
      top: 1964px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 36px;
      line-height: 43px;
      color: #000000;
    }
    .about{
      position: absolute;
      left: 18px;
      top: 2080px;

      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: black;
    }
    .label__name{
      position: absolute;
      width: 30px;
      height: 12px;
      left: -80px;
      top: 2200px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: black;
    }
    #name{
      position: absolute;
      width: 340px;
      height: 50px;
      left: 18px;
      top: 2230px;
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
      top: 2295px;
      left:150px;
      line-height: 12px;
    }
    .label__tel{
      position: absolute;
      width: 49px;
      height: 12px;
      left: -483px;
      top: 2320px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: black;
    }
    #tel{
      position: absolute;
      width: 340px;
      height: 50px;
      left: 18px;
      top: 2340px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px
    }
    .about__advice{
      position: absolute;
      left: 18px;
      top: 2380px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
    }
    .advice{
      position: absolute;
      width: 174px;
      height: 12px;
      left: -80px;
      top: 2490px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    #advice{
      position: absolute;
      width: 340px;
      height: 50px;
      left: 18px;
      top: 2520px;
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
      top: 2580px;
      left:75px;
      line-height: 12px;
    }
    .when{
      position: absolute;
      width: 38px;
      height: 12px;
      left: -480px;
      top: 2610px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
    }
    #when{
      position: absolute;
      width: 340px;
      height: 50px;
      left: 18px;
      top: 2630px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    /*Checkboxes*/
    .connection{
      position: absolute;
      left: 18px;
      top: 2690px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
    }
    /*Section labels*/
    /*viber*/
    .label__viber{
      position: absolute;
      left: 53px;
      top: 2800px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    .span__viber::before{
      content: "";
      position: relative;
      top: 350px;
      left: 125px;
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
    /*Whatsapp*/
    .label__whatsaap{
      position: absolute;
      left: 120px;
      top: 2800px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    .label__mail{
      position: absolute;
      left: 215px;
      top: 2800px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    .label__telephone{
      position: absolute;
      left: 280px;
      top: 2800px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    /*Section inputs*/
    .input__check{
      position: absolute;
      width: 40px;
      height: 40px;
      left: 48px;
      top: 2820px;

      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    #whatsapp{
      position: absolute;
      width: 40px;
      height: 40px;
      left: 128px;
      top: 2820px;

      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    #mail{
      position: absolute;
      width: 40px;
      height: 40px;
      left: 215px;
      top: 2820px;

      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    #telephone{
      position: absolute;
      width: 40px;
      height: 40px;
      left: 290px;
      top: 2820px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    /*second section*/
    .about__us_text{
      position: absolute;
      left: 18px;
      top: 2830px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    /*Second section label*/
    .label__internet{
      position: absolute;
      left: 41px;
      top: 2945px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    .label__recommendation{
      position: absolute;
      left: 110px;
      top: 2945px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    .label__soc{
      position: absolute;
      left: 220px;
      top: 2945px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    .label__alredy_went{
      position: absolute;
      left: 290px;
      top: 2945px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #000000;
    }
    /*Second section input*/
     #internet{
       position: absolute;
       width: 40px;
       height: 40px;
       left: 48px;
       top: 2990px;
       background: #FFFFFF;
       border: 1px solid #E7E7E7;
       box-sizing: border-box;
       border-radius: 3px;
     }
    #recommendation{
      position: absolute;
      width: 40px;
      height: 40px;
      left: 148px;
      top: 2990px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    #soc{
      position: absolute;
      width: 40px;
      height: 40px;
      left: 228px;
      top: 2990px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    #already__went{
      position: absolute;
      width: 40px;
      height: 40px;
      left: 300px;
      top: 2990px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    /*rules*/
    #rss{
      position: absolute;
      width: 15px;
      height: 15px;
      left: 18px;
      top: 3070px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .label__rss{
      position: absolute;
      width: 100%;
      left: 48px;
      top: 3070px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      color: #000000;
    }
    .rss__text{
      position: absolute;
      width: 310px;
      height: 36px;
      left: 48px;
      top: 3090px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #C1C1C1;
    }
    #personal{
      position: absolute;
      width: 15px;
      height: 15px;
      left: 18px;
      top: 3160px;
      background: #FFFFFF;
      border: 1px solid #E7E7E7;
      box-sizing: border-box;
      border-radius: 3px;
    }
    .label__personal{
      position: absolute;
      width: 100%;
      left: 48px;
      top: 3160px;
      font-family: Museo Sans Cyrl,sans-serif;
      font-size: 12px;
      color: #000000;
    }
    .personal__text{
      position: absolute;
      width: 310px;
      height: 36px;
      left: 48px;
      top: 3180px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #C1C1C1;
    }
    .field__text{
      position: absolute;
      width: 310px;
      height: 12px;
      left: 48px;
      top: 3250px;
      font-family: Museo Sans Cyrl, sans-serif;
      font-size: 12px;
      line-height: 12px;
      color: #C1C1C1;
    }
    button{
      position: absolute;
      width: 280px;
      height: 49px;
      left: -453px;
      top: 844px;
    }
  }

</style>
