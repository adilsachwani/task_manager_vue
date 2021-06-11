<template>
    <header>
        <h1>{{title}}</h1>
    </header>
</template>

<script>

import './Button.vue'
import Button from './Button.vue'

export default {
    name: "Header",
    props: ['title'],
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