<template>
<div>
    <h2>{{task}}</h2>
     <button @click="SubTaskAdded">Add a subtask</button>
    <NewSubTask @SubTaskAdded="NewSubTask"/>  

    </div>
</template>
<script>
import NewSubTask from "./NewSubTask.vue"
export default{
    
    name: "Task",
    components:{
        NewSubTask
    },
    props:[
        "task"
    ],
    data(){
        return{
            subtasks:["go to bed"]
        }
    },
    methods:{
        NewSubTask(subtask){
          this.subtasks.push(subtask);
        }
    }



}
</script>
