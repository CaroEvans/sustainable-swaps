<template>
  <div class='banner-container'>
    <div class='lh-banner'>
      <div class='copy-container'>
        <p class='title'>Swap:</p>
        <p class='copy' v-text="left"></p>
      </div>
    </div>
    <div class='rh-banner'>
      <div class='copy-container'>
        <p class='title'>For:</p>
        <p class='copy' v-text="right"></p>
      </div>
    </div >
  </div>
  <button @click="move(1)" type="button">NEXT</button>
</template>

<script>
  export default {
    name: 'HeroBanner',
    props: {
      swaps: {
          type: Object
      }
    },
    data() {
      return {
        index: 0
      }
    },
    computed: {
      left() {
        return this.swaps[this.index].left;
      },
      right() {
        return this.swaps[this.index].right;
      }
    },
    methods: {
      move(change) {
          if (this.swaps[this.index + change]) {
          this.index += change;
          }
    }
}
  };
</script>

<style scoped>


button {
  margin-top: 2rem;
  font-size: 1rem;
  padding: 0.75rem 1rem;
  border: none;
  background-color: #D88C9A;
  color: white;
  font-weight: 600;
  cursor: pointer;
}
button:hover {
    background-color: #F2D0A9;
    color: #2c3e50;
  }

.banner-container {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  padding-left: 1rem;
  padding-right: 1rem;
}
.lh-banner, .rh-banner {
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.copy-container {
  padding: 3rem;
}
.copy, .title {
  font-size: 1.25rem;
  text-align: left;
  margin: 0;
}
.title {
  font-weight: 600;
  display: block;
}
.lh-banner {
  background-color: #D88C9A;
}
.rh-banner {
  background-color: #F2D0A9;
}
.opal {
  color: #99C1B9;
}
.middle-blue-purple {
  color: #8E7DBE;
}
@media screen and (min-width: 46rem) {
  .banner-container {
    flex-direction: row;
  }
  .lh-banner, .rh-banner {
    width: 40vw;
    height: 40vw;
  }
  .copy, .title {
    font-size: 1.5rem;
  }
}
</style>
