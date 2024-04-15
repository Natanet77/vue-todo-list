<template>
  <div>
    <TodoForm @add="addTodo" />
    <ul>
      <li v-for="todo in todos" :key="todo.id" >
        
        <TodoItem :todo="todo" @remove="removeTodo(id)" @toggle="toggleCompleted(id)" />
      </li>
     
    </ul>
    
  </div>
</template>

<script>
import TodoForm from './TodoForm.vue';
import TodoItem from './TodoItem.vue';


export default {
  components: {
    TodoItem,
    TodoForm
  },
  data() {
    return {
    
      todos: [],
      newItemTitle: '',
    };
  },
  methods: {
    addTodo(todo) {
      this.todos.push(todo);
    },
    removeTodo(id) {
      this.todos.splice(id, 1);
    },
    toggleCompleted(id) {
      this.todos[id].completed = !this.todos[id].completed;
    }
  }
};
</script>