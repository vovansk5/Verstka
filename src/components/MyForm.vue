<template>
    <div id="myForm">
    Это компонент форма
    <form name="myForm" action="Get">
      <label> Сок </label>
      <input name="juse" type="checkbox" value="1"> Яблочный
      <input name="juse" type="checkbox" value="1"> Вишневый
      <input name="juse" type="checkbox" value="1"> Грушевый
      <br>


      <label>файл <input type="file" name="file1"></label>

      <br>  
      <label for="animals">Животное </label>
      <select id="animals" name="an" multiple size="3">
        <optgroup label="Крупные">
          <option value="1">Медведь</option>
        </optgroup>
        <option value="2" selected >Заяц</option>
        <option value="3">Лев</option>
      </select>

      <br>  
      <input type="hidden" name="hid" value="100" >

      <br>
      <input type="submit" value="send">
      

      
    </form>

    </div>
</template>

<script>
export default {
    name: 'myForm',
    props: {
        city: String
    }
}
</script>