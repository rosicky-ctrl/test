<template>

<router-link :to="{ name: ''}"></router-link>
<router-view></router-view>

</template>

<script setup>

    import HelloWorld from './components/HelloWorld.vue'

</script>

<style>

    nav a+a {
        margin-left: 1rem;
    }
    nav {
        grid-column: 1/3;
    }

</style>