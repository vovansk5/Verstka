<template>
  <div id="app">
    <MyComp msg="Welcome to Your Vue.js App"/>

    <fieldset>
        <legend>Главное</legend>
        
        <input v-model="firstName" placeholder="Фамилия">
        <br>
        <select v-model="city" multiple>
          <option value="1">Новосибирск</option>
          <option value="2">Барнаул</option>
          <option value="3">Томск</option>
          <option value="4">Москва</option>
        </select>
        
        <br>
        
        <img v-bind:src="imageSrc">
        {{imageSrc}}
        <img src="/MyMedia/1.jpg">

        <br>
        
        <audio v-bind:src="mySound" controls >Послушай меня</audio>
        <audio v-if="numSong==1" src='./assets/appl.mp3' controls >Апплодисменты</audio>
        <audio v-else src='./assets/steps.mp3' controls >Шаги</audio>
        

        <button @click="mySound='/MyMedia/appl.mp3'"> Апплодисменты </button>
        <button @click="mySound='/MyMedia/steps.mp3'"> Шаги </button>
        <button @click="numSongCalc">Следующая песня</button>

        <br>
        Музыка={{mySound}}

    </fieldset>



  </div>
</template>

<script>
import MyComp from './components/MyComp.vue'

export default {
  name: 'App',
  data() {
    return {
    firstName:'Петров',
    city:2,
    imageSrc:"/MyMedia/1.jpg",
    mySound:'./assets/appl.mp3',
    numSong:1}
  },
  methods: {
    numSongCalc() {
      return (this.numSong==2) ? this.numSong=1 : this.numSong=2
    }
  },
  components: {
    MyComp
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
