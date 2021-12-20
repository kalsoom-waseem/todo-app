<template>
<div>
<form>
    <input type="text" v-model='subtask'>
    <button  @click.prevent="createNewSubTask">Add a new SubTask</button>

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
            subtask:''
        }
    },
     methods:{
         createNewSubTask(){
             this.$emit('SubTaskAdded', this.subtask);
             this.subtask ='';
         }
     } 
    
}
</script>
