<template>

    <div :key="task.id" v-for="task in tasks">
        <Task @delete-task="deleteTask" :task="task" />
    </div>

</template>

<script>

import Task from './Task.vue'

export default {
    name: "Tasks",
    props: {
        tasks: Array
    },
    components: {
        Task
    },
    methods: {
        deleteTask(id){
            this.$emit("delete-task", id);
        }
    },
    emits: ['delete-task']
}

</script>