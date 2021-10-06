<template>
  <h1>Sustainable Swaps</h1>
  <HeroBanner itemName="Shampoo in a plastic bottle" swap="Plastic free shampoo bar or dissolvable tablet" />
</template>

<script>
import HeroBanner from './components/HeroBanner.vue'

export default {
  name: 'App',
  components: {
    HeroBanner
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  text-decoration: underline;
  font-size: 2rem;
}
@media screen and (min-width: 46rem) {
  h1 {
    font-size: 3rem;
  }
}
</style>
