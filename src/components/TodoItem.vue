<template>
      <div  >
        <p>
          <span>{{todo}}</span>
          <input type="checkbox" @change="markCompleted"  />
          
          <button @click="removeTodo">x</button>
        </p>
      </div>
</template>

 <script>
    export default {
  
  props: ["todo"],
  data() {
    return {
      todoLocal:this.todo,
      todos: []
      
    };
  },
  methods: {
    
    // markComplete(todo) {
    //   this.todoLocal(todo).completed = !this.todoLocal(todo).completed;
    // },

    // removeTodo(todo) {
    //   this.todos.splice(todo)
    // }
  },
  };
</script>