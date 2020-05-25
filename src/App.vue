<template>
  <div id="app">
    <MyComp msg="Welcome to Your Vue.js App"/>

  </div>
</template>

<script>
import MyComp from './components/MyComp.vue'

export default {
  name: 'App',
  data() {
    return {
    firstName:'Петров'}
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
  margin: 0px;
}
</style>
