<template>
    <header>
        <h1 v-on:click="changeTitle">{{title}}</h1>
    </header>
</template>

<script>
    import {bus} from '../main'
    export default {
        name: "header",
        props:{
            title: {
                type: String
            }
        },
        data(){
            return {
                title: 'Vue Js Web Project'
            }
        },
        methods: {
            changeTitle: function () {
                //this.$emit('changedTitle', 'Vue Js');
                this.title = 'Vue Jssss';
                bus.$emit('titleChanged', 'Vue Js');
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