<template>
    <button @click="$emit('on-click')" class="btn" :style="{background : color}">{{name}}</button>
</template>

<script>
export default {
    name: "Button",
    props: {
        name: String,
        color: String
    }
}
</script>