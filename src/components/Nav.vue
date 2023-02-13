<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
    <nav>
        <div class="container">
            <RouterLink active-class="active" to="/" class="link">Home</RouterLink>
            <RouterLink active-class="active" to="/about" class="link">About</RouterLink>
        </div>
    </nav>
</template>

<style scoped>
.link{
    font-size: 1.3em;
    color: white;
    text-decoration: none;
}

.active{
    font-weight: 900;
    color: black;
}

nav{
    width: 100%;
    padding: 1em;
    background-color: rgba(49, 129, 199, 0.76);
}
.container{
    display: flex;
    width: 30em;
    align-items: center;
    justify-content: space-around;
}

h2{
    color: white;
    cursor: pointer;
}
</style>