<template>
  <div id="app">
  <div class="header">
    To-Do list Application
  </div>
  <div class="frame">
    <parent />
  </div>
  </div>
</template>

<script>

import parent from './components/parent.vue'
export default {
  name: 'App',
  components: {
    parent
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
.header{
  background-color: rgb(108, 155, 108);
  font-family: cursive;
  font-size:30px;
  padding:15px;
  color: aliceblue;

}
.frame{
  border: groove;
  width:400px;
  margin: auto;
  text-align: left;
  margin-top:15px;
   box-shadow: 4px 8px;
}
</style>
