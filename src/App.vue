<!--<template>
    <div>
        <app-header v-bind:title="title" v-on:changedTitle="updateTitle($event)"></app-header>
        <app-content v-bind:omors="omors"></app-content>
        <app-footer v-bind:title="title"></app-footer>
    </div>
</template>

<script>
    import Header from './components/Header.vue';
    import Footer from './components/Footer.vue';
    import Content from './components/Content.vue';

    export default {
        components: {
            'app-header': Header,
            'app-footer': Footer,
            'app-content': Content
        },
        data() {
            return {
                omors: [
                    {name: 'Omor', speciality: 'Laravel', show: false},
                    {name: 'Faruk', speciality: 'CSS', show: false},
                    {name: 'Sazzad', speciality: 'HTML', show: false},
                    {name: 'Sunve', speciality: 'PHP', show: false},
                    {name: 'Mahmud', speciality: 'Python', show: false},
                    {name: 'Abubakkar', speciality: 'SEO', show: false}
                ],
                title: 'Vue Js Tutorial'
            }
        },
        methods: {
            updateTitle: function (updateTitle) {
                this.title = updateTitle;
            }
        }
    }
</script>

<style scoped>

</style>-->


<!--Slot Practice-->

<template>
    <div>
        <form-helper>
            <div slot="form-header">
                <h3>This is the title of the Form</h3>
                <p>Information about the form</p>
            </div>
            <div slot="form-fields">
                <input type="text" placeholder="name" required/>
                <input type="password" placeholder="password" required/>
            </div>
            <div slot="form-controls">
                <button v-on:click="handleSubmit">Submit</button>
            </div>
        </form-helper>
    </div>
</template>

<script>

    import FormHelper from './components/FormHelper';
    export default {
        components: {
            FormHelper,
            'form-helper': FormHelper
        },
        data() {
            return {}
        }
    }
</script>

<style scoped>

</style>