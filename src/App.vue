<script setup>
import HomeView from "./views/HomeView.vue";
import AboutView from "./views/AboutView.vue";
import { RouterView } from "vue-router";
import Nav from "./components/Nav.vue";
import { ref } from "vue";

const randomState = ref("");
</script>

<template>
  <div>
    <Nav />
    <RouterView />
  </div>
</template>
