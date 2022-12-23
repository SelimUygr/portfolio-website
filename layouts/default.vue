<template>
  <div style="position: relative; z-index: 1">
    <appHeader />
    <Nuxt />
    <appFooter />
    <div class="cursor">
      <div class="cursor__txt"></div>
      <div class="cursor__icon"></div>
    </div>
  </div>
</template>

<script>
import appHeader from "../components/common/appHeader.vue";
import appFooter from "../components/common/appFooter.vue";

import gsap from "gsap";

export default {
  components: {
    appHeader,
    appFooter,
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start();
      setTimeout(() => this.$nuxt.$loading.finish(), 1000);
    });
    const cursor = document.querySelector(".cursor");
    const dragMoveField = document.querySelectorAll(".js-drag-move-field");
    const linkField = document.querySelectorAll(".js-link-field");

    dragMoveField.forEach((e) => {
      e.addEventListener("mouseenter", () => {
        cursor.classList.add("is-drag");
        let cursorText = e.getAttribute("data-cursor-text");
        cursor.querySelector(".cursor__txt").innerHTML = cursorText;
      });
      e.addEventListener("mouseleave", () => {
        cursor.classList.remove("is-drag");
      });
    });
    linkField.forEach((e) => {
      e.addEventListener("mouseenter", () => {
        cursor.classList.add("is-link");
        let cursorText = e.getAttribute("data-cursor-text");
        cursor.querySelector(".cursor__txt").innerHTML = cursorText;
      });
      e.addEventListener("mouseleave", () => {
        cursor.classList.remove("is-link");
        cursor.querySelector(".cursor__txt").innerHTML = "";
      });
    });
    gsap.set(cursor, {
      xPercent: -50,
      yPercent: -50,
    });
    document.addEventListener("pointermove", movecursor);
    function movecursor(e) {
      gsap.to(cursor, {
        duration: false,
        x: e.clientX,
        y: e.clientY,
        duration: 0.5,
        ease: "slow",
      });
    }
  },
};
</script>

AppHeader
