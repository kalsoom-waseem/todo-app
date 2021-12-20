<template>
<div>
<form>
    <input type="text" v-model='newTask'>
    <button  @click.prevent="createNew">Add a new Task</button>

</form>
    </div>
</template>
<script>


export default{
    
    name: 'NewTask',
    components:{ 
    },
    data(){
        return{
            newTask:''
        }
    },
     methods:{
         createNew(){
             this.$emit('TaskAdded', this.task);
             this.task ='';
         }
     } 
    
}
</script>
