<template>
  <div id="app">
    <Header />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"></Todos>
  </div>
</template>

<script>
import Todos from './components/Todos'
import Header from './components/layout/Header'

export default {
  name: 'app',
  components: {
    Header,
    Todos,
  },
  data(){
    return{
      todos: [
        {
          id: 1,
          title: "To do 1",
          completed: false
        },
        {
          id: 2,
          title: "To do 2",
          completed: false
        },
      ]
    }
  },
  methods: {
    deleteTodo(id){
      this.todos = this.todos.filter(todo => todo.id !== id);
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
