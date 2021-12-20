<template>
  <div >
      
      <input  @keyup.enter="addTodo" class='todo-input' placeholder="What needs to be done" v-model="newTodo"  >
      <button @click="addTodo()">Submit</button>
      <div v-for ="todo in todos" :key ='todo.index' class="todo-item">
      <input type="checkbox" v-model="todo.completed">
      <div>{{todo.title}}</div>
      <div class="remove-item" @click="removeTodo">
        &times;
      </div>
       </div>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  props: {
    msg: String
  },
  data(){
      return{
        newTodo: '',
        idforTodo: 3,
        todos:[
            {
                id:1,
                title: "nothing",
                completed: false,
                 
            },
            {
                id:2,
                title: "nothing 2",
                completed: false,
                 
            },
        ]   
      }
  },
  methods:{
    addTodo(){
      console.log('nothing')
      if(this.newTodo.trim().length==0){
        return

      }
      
     this.todos.push({
        id:this.idforTodo,
        title:this.newTodo,
        completed:false,

     })
     this.newTodo ='',
     this.idforTodo++
    },
    removeTodo(index){
     this.todos.splice(index,1)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.todo-input{
width: 50%;
font-size: 18px;
margin-bottom:16px;
padding: 10 10px;
}
.todo-item{
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  justify-content: space-between
}
.remove-item{
  cursor: pointer;
  margin-left: 14px;
  
}


</style>
