<template>
  <div id="app" class='container'>
    <img alt="Vue logo" src="./assets/logo.png">
    <TodoList/>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'


export default {
  name: 'App',
  components: {
    TodoList
  }
}
</script>

<style>
* {
 box-sizing: border-box;
}
.container{
  margin: 0 auto;
  max-width: 600px;
  border: 20px solid black;
  padding: 20 px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  font-size: 24px;
}
</style>
