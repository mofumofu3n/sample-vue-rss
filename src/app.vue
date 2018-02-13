<template>
    <div>
        <h1>{{ msg }}</h1>
        <clock></clock>
    </div>
</template>

<script>
    import Clock from './components/clock.vue'

    export default {
        data () {
            return {
                msg: 'Welcome to Vue.js'
            }
        },
        components: {
            Clock
        }
    }
</script>

<style>
</style>