<template>

<router-link :to="{ name: ''}"></router-link>
<router-view></router-view>

</template>

<script setup>

    import { ref } from 'vue'
    let products = ref(null)
    fetch('https://api.nbp.pl/api/exchangerates/tables/a/?format=json')
    .then (response => response.json())
    .then (data => products.value = data)
    import HelloWorld from './components/HelloWorld.vue'

</script>

<style>

    table.products {
        width: 100%;
        border-collapse: collapse;
    }
    table.products td, table.products th {
        padding: 1rem;
        border: 2px solid black;
    }
    nav a+a {
        margin-left: 1rem;
    }
    nav {
        grid-column: 1/3;
    }

</style>
