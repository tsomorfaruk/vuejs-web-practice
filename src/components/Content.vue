<template>
    <div id="omors">
        <ul>
            <li v-for="omor in omors" v-on:click="omor.show = !omor.show">
            <h2>{{omor.name}}</h2>
            <h3 v-show="omor.show">{{omor.speciality}}</h3></li>
        </ul>
        <button v-on:click="deleteTable">Delete Table</button>
    </div>
</template>

<script>
    export default {
        name: "content",
        props: {
            omors: {
                type: Array,
                required: true
            }
        },
        data() {
            return {

            }
        },
        methods: {
            deleteTable: function () {
                this.omors.pop();
            }
        }
    }
</script>

<style scoped>
    #omors{
        width: 100%;
        max-width: 1200px;
        margin: 4px auto;
        padding: 0 20px;
        box-sizing: border-box;
    }
    ul{
        display: flex;
        flex-wrap: wrap;
        list-style-type: none;
        padding: 0;
    }
    li{
        flex-grow: 1;
        flex-basis: 300px;
        text-align: center;
        padding: 30px;
        border: 1px solid #222;
        margin: 10px;
    }
</style>