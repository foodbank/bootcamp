<template>
    <div class="container">
        <button :class="{ 'is-landing': isLanding }" @click="toggleClass">Hello world</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                className: 'color-red',
                isLanding: true
            }
        },
        methods: {
            toggleClass () {
                if (this.isLanding) {
                    this.isLanding = false;
                } else {
                    this.isLanding = true;
                }
            }
        }
    }
</script>

<style lang="scss">
    .is-landing { color: red; }
</style>
