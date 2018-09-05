<template>
    <header>
        <h1>{{title}}</h1>
    </header>
</template>

<script>
    export default {
        name: "header",
        data(){
            return {
                title: 'Vue Js Web Project'
            }
        }
    }
</script>

<style scoped>
    header{
        background: lightgreen;
        padding: 10px;
        border: 2px solid #222;
    }
    h1{
        color: #222;
        text-align: center;
    }
</style>