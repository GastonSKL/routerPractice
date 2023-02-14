<script setup>
import cars from '../data/Cars.json';
import { RouterLink } from 'vue-router';
</script>

<template>
    <div class="container">
        <h1>Car list</h1>
        <div class="links">
            <div class="cars"> 
                <RouterLink v-for="car in cars" href="" class="link" :to="`/cars/${car.id}`" >{{car.name}}</RouterLink>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container{
    text-align: center;
}

.container h1{
    text-transform: uppercase;
    margin: 1em 0;
}
.links{
    width: 62em;
    margin: 0 auto;
    padding: 1em;
}

.cars{
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.cars .link{
    font-size: 1.3em;
    text-decoration: none;
    cursor: pointer;
    box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.281);
    padding: .5em;
    border-radius: .8em;
}
</style>