<template>
  <div class='banner-container'>
    <div class='lh-banner'>
      <p class='copy'>
        <span class='title'>Swap:</span>
        {{ itemName }}
      </p>
    </div>
    <div class='rh-banner'>
      <p class='copy'>
        <span class='title'>For:</span>
        {{ swap }}
      </p>
    </div >
  </div>
</template>

<script>
export default {
  name: 'HeroBanner',
  props: ['itemName', 'swap']
};
</script>

<style scoped>

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
.copy {
  font-size: 1.25rem;
  text-align: left;
  padding: 3rem;
}
.title {
  font-weight: 600;
  display: block;
  text-decoration: underline;
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
  .copy {
    font-size: 1.5rem;
  }
}
</style>
