<template>
<div  class="aside__main">
  <select class="aside__select" name="Страны" id="с">
    <option value="c">Страны :</option>
    <optgroup label="Южная Америка"  selected>
      <option>Аргентина</option>
      <option>Бразилия</option>
      <option>Перу</option>
      <option>Уругвай</option>
      <option>Чили</option>
      <option>Эквадор</option>
    </optgroup>
    <optgroup label="Северная Америка">
      <option>Аргентина</option>
      <option>Бразилия</option>
      <option>Перу</option>
      <option>Уругвай</option>
      <option>Чили</option>
      <option>Эквадор</option>
    </optgroup>
    <optgroup label="Арктика и Антарктика">
      <option>Аргентина</option>
      <option>Бразилия</option>
      <option>Перу</option>
      <option>Уругвай</option>
      <option>Чили</option>
      <option>Эквадор</option>
    </optgroup>
    <optgroup label="Африка">
      <option>Аргентина</option>
      <option>Бразилия</option>
      <option>Перу</option>
      <option>Уругвай</option>
      <option>Чили</option>
      <option>Эквадор</option>
    </optgroup>
    <optgroup label="Австралия и океания">
      <option>Аргентина</option>
      <option>Бразилия</option>
      <option>Перу</option>
      <option>Уругвай</option>
      <option>Чили</option>
      <option>Эквадор</option>
    </optgroup>
    <optgroup label="Европа">
      <option>Аргентина</option>
      <option>Бразилия</option>
      <option>Перу</option>
      <option>Уругвай</option>
      <option>Чили</option>
      <option>Эквадор</option>
    </optgroup>
    <optgroup label="Россия">
      <option>Аргентина</option>
      <option>Бразилия</option>
      <option>Перу</option>
      <option>Уругвай</option>
      <option>Чили</option>
      <option>Эквадор</option>
    </optgroup>
    <optgroup label="Азия">
      <option>Аргентина</option>
      <option>Бразилия</option>
      <option>Перу</option>
      <option>Уругвай</option>
      <option>Чили</option>
      <option>Эквадор</option>
    </optgroup>
  </select>
  <div  class="date__aside">
  <input type="text"
         id="date__aside"
         placeholder="Даты"
         onfocus="(this.type='date')"
         onblur="(this.type='text')" required>
  </div>
  <div class="type__adventure">
    <select name=""  id="t">
      <option value="t">Тип путешествия: </option>
      <option value="">Активный</option>
      <option value="">Майские</option>
      <option value="">На Авто</option>
      <option value="">На корабле</option>
      <option value="">Новый год</option>
      <option value="">Поход</option>
      <option value="">Сёрфинг</option>
      <option value="">Экзклюзив</option>
      <option value="">Экскурсионный</option>
      <option value="">Экспедиция</option>
    </select>
  </div>
  <div class="aside__list">
    <ul>
      <li><a href="#">Путешествия</a></li>
      <li><a href="#">О нас</a></li>
      <li><a href="#">Отзывы</a></li>
      <li><a href="#">Блог</a></li>
    </ul>
  </div>

  <div  class="aside__text">
    <p>
      8 (800) 123-45-67
    </p>
  </div>
  <div class="aside__btn">
       <button>Подберите мне тур</button>
  </div>
</div>
</template>

<script>

export default {
  data() {
    return {
      data: {
        type: Number,
      },
    };
  },
  name: 'SideInfoTour',
};
</script>

<style scoped lang=scss>
  @font-face {
    font-family: Museo Sans Cyrl;
    src: url('../assets/fonts/Museo Sans Cyrl.ttf') format('opentype');
  }
select{
  z-index:20000 ;
  -webkit-appearance: none;
  font-family: Museo Sans Cyrl,sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 14px;
  color: #000000;
}
select:focus{
  outline:none;
  background-image:url("../assets/img/aside-forms.png");
  background-repeat: no-repeat;
  background-position-x:110px;
  background-position-y:20px ;
}
  .aside__main{
    display: flex;
    flex-direction: column;
  }
  .aside__select{
    position: absolute;
    width: 150px;
    height: 49px;
    left: 0;
    top: 100px;

    background: #FFFFFF;
    border-radius: 30px;
    padding-left: 30px;
    margin-left: 120px;
  }
  #date__aside{
    font-family: Museo Sans Cyrl,sans-serif;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 14px;
    color: #000000;
    position: absolute;
    width: 120px;
    height: 49px;
    left: 277px;
    top: 101px;
    outline: none;

    background: #FFFFFF;
    border-radius: 30px;
    padding-left: 30px;
    border: 1px solid #272727;
  }
  ::-webkit-calendar-picker-indicator {
    color: transparent;
    background:
      url("../assets/img/aside-forms.png")
      no-repeat center;
    background-size: 9px;
    z-index:300000 ;
    padding-right: 25px;
    width: 2px;
  }
  #t{
    position: absolute;
    width: 280px;
    height: 49px;
    left: 135px;
    top: 168px;

    background: #FFFFFF;
    border-radius: 30px;
    padding-left: 30px;
  }
  #t:focus{
    outline:none;
    background-image:url("../assets/img/aside-forms.png");
    background-repeat: no-repeat;
  }
  .aside__list{
    position: absolute;
    width: 157px;
    height: 153px;
    left: 176px;
    top: 285px;

    font-family: Museo Sans Cyrl, sans-serif;
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    line-height: 22px;
    text-align: center;
    letter-spacing: 0.1em;
  }
  ul{
    list-style: none;
  }
  li{
    padding-top:15px;
  }
  a{
    text-decoration: none;
    color: #141414;
  }
</style>
