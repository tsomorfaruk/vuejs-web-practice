<template>
    <footer>
        <p>{{copyright}}</p>
    </footer>
</template>

<script>
    export default {
        name: "footer",
        data(){
            return {
                copyright: 'Copyright 2018 Omor Faruk'
            }
        }
    }
</script>

<style scoped>
    footer{
        background: #222;
        padding: 6px;
        border: 2px solid lightgreen;
    }
    p{
        color: lightgreen;
        text-align: center;
    }
</style>