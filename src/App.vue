<template>
  <div id="app">
    <h1>{{title}}</h1>
    <TodoList />
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue';

export default {
  data() {
    return {
      title: "TODO list"
    };
  },
  
  components: {
    TodoList
  }
};
</script>

<style>
#app {
 
  text-align: center;
  color: #2c3e50;
  margin-top: 40px;
}
</style>
