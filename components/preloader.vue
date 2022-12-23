<template>
  <div
    v-if="this.loading"
    class="preloader"
    ref="preloader"
    :class="this.loading == false ? 'loaded' : ''"
  ></div>
</template>

<script>
export default {
  data() {
    return {
      loading: null,
    };
  },
  methods: {
    start() {
      this.loading = true;
    },
    finish() {
      this.$refs.preloader.classList.add("loaded");
      setTimeout(() => {
        this.loading = false;
      }, 1000);
    },
  },
};
</script>

<style scoped lang="scss">
.preloader {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at center, transparent 0.1%, #000000 0.1%);
  text-align: center;
  font-family: sans-serif;
  z-index: 99;
  transition: var(--transition);
  &.loaded {
    transform: scale(1000);
  }
}
</style>
