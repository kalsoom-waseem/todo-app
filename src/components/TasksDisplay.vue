<template>
<div>
<div :key="task.id" v-for="task in tasks">

    <app-task  :task="task" >
      
    </app-task>
    </div>
    </div>
</template>
<script>
import Task from './Task.vue'
export default{
    name: 'TasksDisplay',
    components:{
      appTask: Task
    },
    data(){
      return{
        subtask:''
      }
    },
    props: ["tasks"],
    methods:{
    
    },
      
    
}
</script>
