<script setup>
import { useRoute, RouterView, useRouter } from "vue-router";
import cars from "../data/Cars.json";
import ContactView from "./ContactView.vue";
const route = useRoute();
const router = useRouter();
const cardId = parseInt(route.params.id);
const car = cars.find((car) => car.id === parseInt(route.params.id));

console.log(car);
</script>

<template>
  <main>
    <div class="container" v-if="car">
      <h1>{{ car.name }}</h1>
      <p>{{ car.year }}</p>
      <div class="container__info">
        <img :src="car.img" class="container__info-img" />
        <p class="container__info-price">{{ car.price }}$</p>
        <button @click="router.push(`/cars/${cardId}/contact`)">
          Contact!
        </button>
      </div>
      <RouterView class="contact" />
    </div>
    <dir v-else>
        <h1 >Car not found</h1>
    </dir>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  display: grid;
  place-content: center;
}
.container {
  width: 19em;
  height: 25em;
  padding: 2em;
  background-color: rgba(149, 149, 253, 0.479);
  border-radius: 0.8em;
}

.container h1 {
  font-weight: bolder;
  margin-bottom: 0.5em;
  text-transform: uppercase;
}

.container p {
  font-size: 0.9em;
  margin-bottom: 0.5em;
}

.container__info {
  height: 15em;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.container__info img {
  border: 1px solid black;
  height: 80%;
  width: 15em;
  border-radius: 0.4em;
}

.container__info p {
  font-weight: bolder;
  letter-spacing: 0.2em;
}
.contact {
  width: 10em;
  height: 6em;
  background-color: rgb(149, 149, 253);
}
</style>
