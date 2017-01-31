<template>
    <div class="container">
        <input type="text" v-model="message">
        <p>message: {{ message }}</p>
    </div>
</template>

<script>
    export default {
        data() {
            return { message: 'Hello world' }
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>

<style lang="scss">
    .container {
        color: darkseagreen;
    }
</style>
