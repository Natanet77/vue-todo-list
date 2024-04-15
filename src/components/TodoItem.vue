 <template>
      <div  >
        <p>
           <span>{{todo}}</span>
          <input type="checkbox" @change="markCompleted"  />
          
          <button @click="deleteTodo">x</button>
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
    
    markComplete(id) {
      this.todoLocal(id).completed = !this.todoLocal(id).completed;
    },

    
  },
};
    </script>