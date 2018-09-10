<template>
    <div>
        <add-blog>
        </add-blog>
    </div>
</template>

<script>
    import addBlog from './components/addBlog.vue';
    import AddBlog from "./components/addBlog";
    export default {
        components: {
            AddBlog,
            'add-blog': addBlog
        },
        data() {
            return {}
        }
    }
</script>

<style scoped>
    body{
        margin: 0;
        font-family: Nunito SemiBold;
    }
</style>