<template>
    <button @click="onClick()" class="btn" :style="{background : color}">{{name}}</button>
</template>

<script>
export default {
    name: "Button",
    props: {
        name: String,
        color: String
    },
    methods: {
        onClick(){
            console.log("click");
        }
    }
}
</script>