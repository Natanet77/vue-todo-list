<template>
  <div>
    <input type="text" v-model="newItemTitle" placeholder="Type new item...">
    <button @click="addTodo">Add</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [],
      newItemTitle: ''
    };
  },
  methods: {
    addTodo() {
           this.$emit('add', this.newItemTitle, {completed: false} );
      // this.newItemTitle = '';
      // this.todos.push({
      //   id: this.id,
      //   text: this.newItemTitle,
      //   completed: false,
      // });
      
      this.newItemTitle = '';
    }
    
  }
};
</script>