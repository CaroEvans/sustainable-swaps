<template>
  <button @click="move(1)" type="button">NEXT</button>
  <div class="banner-container">
    <div class="lh-banner">
      <div class="copy-container">
        <p class="title">Swap:</p>
        <p class="copy" v-text="left"></p>
      </div>
    </div>
    <div class="rh-banner">
      <div class="copy-container">
        <p class="title">For:</p>
        <p class="copy" v-text="right"></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroBanner",
  props: {
    swaps: {
      type: Object,
    },
  },
  data() {
    return {
      index: 0,
    };
  },
  computed: {
    left() {
      return this.swaps[this.index].left;
    },
    right() {
      return this.swaps[this.index].right;
    },
  },
  methods: {
    move(change) {
      if (this.swaps[this.index + change]) {
        this.index += change;
      }
    },
  },
};
</script>
