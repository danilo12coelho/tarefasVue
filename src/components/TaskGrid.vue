<template>
    <div class="task-grid">
        <task v-for="task in tasks" :key="task.name" :task='task'/>
    </div>
</template>

<script>  
import Task from './Task.vue'  
export default{
    
    components:{Task},

    props: {
        tasks: {type: Array, required: true}
    }

}
</script>