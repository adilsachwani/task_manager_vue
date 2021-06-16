<template>
    <header>
        <h1>{{title}}</h1>
        <Button 
            v-show="homePage"
            @on-click="$emit('toggle-add-task')"
            :name="showAddTask ? 'Close' : 'Add Task'"
            :color="showAddTask ? 'red' : 'green'" />
    </header>
</template>

<script>

import Button from './Button.vue'

export default {
    name: 'Header',
    props: {
        title: {
            type: String
        },
        showAddTask: {
            type: Boolean
        }
    },
    components: {
        Button
    },
    computed: {
        homePage(){
            if(this.$route.path == '/'){
                return true
            } else {
                return false
            }
        }
    }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>