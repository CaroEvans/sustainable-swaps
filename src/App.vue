<template>
  <h1>Sustainable Swaps</h1>
  <HeroBanner :swaps="[
    {left: 'Shampoo in a plastic bottle', right: 'Shampoo bar or dissolvable tablet' },
    {left: 'Conditioner in a plastic bottle', right: 'Conditioner bar or dissolvable tablet' },
    {left: 'Face cleanser in a plastic bottle', right: 'Face cleanser bar or dissolvable tablet' },
    {left: 'Exfoliator in a plastic bottle', right: 'Exfoliator bar' },
    {left: 'Plastic clothes pegs', right: 'Stainless steel or wooden pegs'},
    {left: 'Lip balm in a plastic tube', right: 'Lip balm in cardboard tube'},
    {left: 'Deodorant/antiperspirant in a plastic tube', right: 'Plastic free solid bar, cardboard tube or recyclable metal tin'},
  ]"/>
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
h1:hover {
  color: #D88C9A;
}
@media screen and (min-width: 46rem) {
  h1 {
    font-size: 3rem;
  }
}
</style>
