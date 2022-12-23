<template>
  <headroom
    :speed="400"
    :upTolerance="10"
    :downTolerance="10"
    :classes="{
      pinned: 'header--pinned',
      unpinned: 'header--unpinned',
      top: 'header--top',
      notTop: 'header--not-top',
    }"
  >
    <header ref="header" class="header">
      <div class="container">
        <div class="header__wrapper">
          <div class="header__logo">
            <img src="~/static/images/buffalo-logo.svg" alt="" />
          </div>
          <div @click="openMenu" class="header__menu-btn">
            <div class="header__menu-btn-line"></div>
            <div class="header__menu-btn-line"></div>
          </div>
          <div ref="headerMenu" class="header__menu">
            <div class="header__menu__item c-white txt txt--rem24 txt--font400">
              <NuxtLink to="/">Home</NuxtLink>
            </div>
            <div class="header__menu__item c-white txt txt--rem24 txt--font400">
              <NuxtLink to="/about">About</NuxtLink>
            </div>
            <div class="header__menu__item c-white txt txt--rem24 txt--font400">
              <NuxtLink to="/works">Works</NuxtLink>
            </div>
            <div class="header__menu__item c-white txt txt--rem24 txt--font400">
              <NuxtLink to="/contact">Contact</NuxtLink>
            </div>
          </div>
        </div>
      </div>
    </header>
  </headroom>
</template>

<script>
import { headroom } from "vue-headroom";

export default {
  components: { headroom },
  methods: {
    openMenu(e) {
      const header = this.$refs.header;
      const headerMenu = this.$refs.headerMenu;
      headerMenu.classList.toggle("opened");
      header.classList.toggle("menu-opened");
    },
  },
};
</script>
