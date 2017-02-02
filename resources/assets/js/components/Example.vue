<template>
    <div class="container">
        <ul>
            <li v-for="name in names" v-text="name"></li>
        </ul>
        <input id="input" type="text" v-model="newName">
        <button id="button" @click="addName">Add new username</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                newName: '',
                names: ['Joe', 'Mary', ' Jack']
            }
        },
        methods: {
            addName () {
                this.names.push(this.newName);
                this.newName = '';
            }
        },
        mounted() {
        }
    }
</script>

<style lang="scss">
    .container {
        color: darkseagreen;
    }
</style>
