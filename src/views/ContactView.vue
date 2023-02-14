<script setup>
import { useRoute } from 'vue-router';
import cars from "../data/Cars.json"
const route = useRoute();
const car = cars.find(c=>c.id === parseInt(route.params.id));
</script>

<template>
    <div class="container">
        <h1>Seller</h1>
        <p>{{car.contact.dealer}}</p>
        <p>{{car.contact.number}}</p>
    </div>
</template>

<style scoped>
.container{
    position: absolute;
    width: 5em;
    height: 6em;
    top: 21em;
    left: 36.5em;
    border: 1px solid black;
}

.container h1{
    font-size: 1em;
    color: green;
    font-weight: bolder;
    margin-bottom: .5em;
    margin-top: -1.3em;
}

.container p{
    font-size: .9em;
    margin: .5em 0em;
}
</style>