<template>
    <div class="container">
        <ul>
            <li v-for="name in names" v-text="name"></li>
        </ul>
        <input id="input" type="text">
        <button id="button">Add new username</button>
    </div>
</template>

<script>
    export default {
        data() {
            return { names: ['Joe', 'Mary', ' Jack'] }
        },
        mounted() {
            document.querySelector("#button").addEventListener('click', () => {
                let name = document.querySelector("#input");

                console.log(this.$data.names.push(name.value));

                name.value = '';
            });
        }
    }
</script>

<style lang="scss">
    .container {
        color: darkseagreen;
    }
</style>
