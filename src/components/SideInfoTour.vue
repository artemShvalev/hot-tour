<template>
<div  class="aside__main">
  <select name="Страны" id="">
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
  <input type="date" name="date" id="when" value="..." placeholder="Дата" required>
  </div>
  <div  class="type__adventure">
    <select name="">
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
select{
  z-index:20000 ;
}
</style>
