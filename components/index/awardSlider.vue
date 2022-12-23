<template>
  <section class="section award-slider">
    <div class="container">
      <div
        class="award-slider__wrapper row g-4 g-md-5 align-items-center c-white flex-column-reverse flex-lg-row"
      >
        <div class="award-slider__text col-12 col-lg-5">
          <div ref="textSlider" class="swiper">
            <div class="swiper-wrapper">
              <div
                v-for="(slide, index) in awardSlider"
                :key="index"
                class="swiper-slide"
              >
                <NuxtLink
                  :to="{
                    path: `work-detail/${slide.title
                      .toLowerCase()
                      .replace(/ /g, '-')}`,
                  }"
                  class="award-slider__text-item"
                  :class="slide ? 'js-link-field' : ''"
                  data-cursor-text="View Project"
                >
                  <div
                    class="award-slider__text-item__title txt txt--rem64 txt--font900 c-white"
                  >
                    {{ slide.title }}
                  </div>
                  <div
                    class="award-slider__text-item__subtitle txt txt--rem28 txt--font300 c-paragraph"
                  >
                    {{ slide.type }}
                  </div>
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>
        <div
          class="award-slider__right col-12 col-lg-7 js-drag-move-field c-none"
          data-cursor-text="Drag"
        >
          <div ref="thumbSlider" class="swiper">
            <div class="swiper-wrapper">
              <div
                v-for="(slide, index) in awardSlider"
                :key="index"
                class="swiper-slide"
              >
                <div class="award-slider__right-item">
                  <div class="award-slider__right-item__image">
                    <div class="award-image">
                      <img :src="slide.awardImage" alt="" />
                    </div>
                    <div class="award-slider__right-item__image-wrapper">
                      <img :src="slide.image" alt="" />
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// import { mapState, mapGetters } from "vuex";

import { Swiper, Thumbs, Autoplay } from "swiper";
Swiper.use([Thumbs, Autoplay]);
export default {
  data() {
    return {
      awardSlider: [
        {
          title: "Trowas",
          type: "Altın Örümcek Finalist",
          awardImage: "images/orumcek.png",
          image: "images/work-trowas.png",
        },
        {
          title: "Chace People",
          type: "Kristal Elma Silver Award",
          awardImage: "images/kristal.png",
          image: "images/work-chace.png",
        },
        {
          title: "Latro",
          type: "Horizon Silver Award",
          awardImage: "images/horizon.png",
          image: "images/work-latro.png",
        },
      ],
    };
  },
  mounted() {
    this.$nextTick(() => {
      const swiperText = new Swiper(this.$refs.textSlider, {
        loop: false,
        direction: "vertical",
        slidesPerView: 1,
        speed: 1000,
        watchSlidesProgress: true,
        watchSlidesVisibility: true,
        breakpoints: {
          320: {
            direction: "horizontal",
            spaceBetween: 75,
            slidesPerView: 1,
          },
          991: {
            direction: "vertical",
          },
        },
      });

      const swiperThumb = new Swiper(this.$refs.thumbSlider, {
        loop: false,
        modules: [Thumbs],
        slidesPerView: 1,
        speed: 1000,
        direction: "vertical",
        thumbs: {
          swiper: swiperText,
        },
        breakpoints: {
          320: {
            direction: "horizontal",
            spaceBetween: 75,
            slidesPerView: 1,
          },
          991: {
            direction: "vertical",
          },
        },
      });
    });
  },
};
</script>
