<template>
   <div>
     <div class="form__title">
       <h3>Заявка на подбор путешествия</h3>
     </div>
     <div class="about">
       <p>НЕМНОГО О ВАС</p>
     </div>
     <div class="first__form">
       <label for="name">Имя<span class="required">*</span><input type="text" name="name" id="name">
       </label>
       <label for="tel">Телефон<input type="tel" name="name" id="tel" placeholder="+7___ ___ __ __">
       </label>
     </div>
     <div class="about__advice">
        <p>О ПУТЕШЕСТВИИ</p>
     </div>
     <div class="second__form">
       <label for="advice">Куда и когда хотите поехать<span class="required">*</span>
         <input type="text" name="name" id="advice" placeholder="Континент, страна или город" >
       </label>
       <label for="when">Когда?
         <input type="date" name="date" id="when" placeholder="Даты или временной  интервал">
       </label>
     </div>
     <div class="connection">
       <p>Удобный способ связи</p>
     </div>
     <div class="checked">
       <label for="viber">Viber</label>
       <input type="checkbox" id="viber">

       <label for="watsapp">WhatsApp</label>
       <input type="checkbox" id="watsapp">

       <label for="mail">Почта</label>
       <input type="checkbox" id="mail">

       <label for="telephone">Телефон</label>
       <input type="checkbox" id="telephone">
     </div>
     <div class="about us">
       <label for="internet">Интернет</label>
       <input type="checkbox" id="internet">

       <label for="recommendation">Рекомендовали друзья</label>
       <input type="checkbox" id="recommendation">

       <label for="soc">Соц.сети</label>
       <input type="checkbox" id="soc">

       <label for="already went">Уже ездил</label>
       <input type="checkbox" id="already went">
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

<style scoped>

</style>
