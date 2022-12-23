<template>
  <main class="detail-page">
    <div class="container container--fluid">
      <div class="subheader">
        <div class="subheader__title txt txt--rem128 txt--font900 c-white">
          <h1>My <span class="c-primary">Works</span></h1>
        </div>
      </div>
    </div>
    <section class="section works">
      <div class="container container--fluid">
        <div class="row g-4 g-md-5">
          <div
            class="col-12 col-lg-6 col-xxl-4"
            v-for="(item, index) in workList"
            :key="index"
          >
            <NuxtLink
              :to="{
                path: `work-detail/${item.title
                  .toLowerCase()
                  .replace(/ /g, '-')}`,
              }"
              class="works-card"
            >
              <div class="works-card__image">
                <img :src="item.image" alt="" />
              </div>
              <div class="works-card__content">
                <div class="works-card__content-title">
                  <h3 class="txt txt--rem32 txt--font900 c-white">
                    {{ item.title }}
                  </h3>
                  <p class="txt txt--rem20 txt--font300 c-white">
                    {{ item.type }}
                  </p>
                </div>
                <div class="works-card__content-button c-white">
                  <svg-icon name="iconArrow" />
                </div>
              </div>
            </NuxtLink>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  data() {
    return {
      workList: [
        {
          title: "Chace People",
          type: "Business & Corporate Website",
          image: "images/chace-banner.png",
        },
        {
          title: "Trowas Exe",
          type: "QR Generator & Card Desing Application",
          image: "images/trowas-exe-cover.png",
        },
        {
          title: "Trowas",
          type: "E-Commerce Website",
          image: "images/trowas-cover.png",
        },
        {
          title: "Alfamak CMS",
          type: "Website CMS",
          image: "images/alfamak-panel-cover.png",
        },
        {
          title: "Latro",
          type: "Corporate Website",
          image: "images/latro-cover.png",
        },
        {
          title: "Trowas Digital Card",
          type: "Digital Business Card Website",
          image: "images/trowas-mobile-cover.png",
        },
        {
          title: "Tansu Yacht",
          type: "Corporate Website",
          image: "images/tansu-cover.png",
        },
        {
          title: "Yasalar",
          type: "Corporate Website",
          image: "images/yasalar-cover.png",
        },
      ],
    };
  },
};
</script>
