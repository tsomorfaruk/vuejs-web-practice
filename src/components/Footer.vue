<template>
    <footer>
        <p>{{copyright}} {{title}}</p>
    </footer>
</template>

<script>
    import {bus} from '../main';
    export default {
        name: "footer",
        props: {
            title: {
                type: String
            }
        },
        data(){
            return {
                copyright: 'Copyright 2018'
            }
        },
        created() {
            bus.$on('titleChanged', (data) =>{
                this.title = data;
            })
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