<template>
  <main>
    <hero />
    <works />
    <about />
    <awardSlider />
  </main>
</template>

<script>
import hero from "../components/index/hero.vue";
import works from "../components/index/works.vue";
import about from "../components/index/about.vue";
import awardSlider from "../components/index/awardSlider.vue";
export default {
  components: { hero, works, about, awardSlider },
};
</script>

<style lang="scss"></style>
