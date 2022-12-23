<template>
  <main class="detail-page">
    <div class="container">
      <div class="subheader">
        <div class="subheader__title txt txt--rem128 txt--font900 c-white">
          <h1>Chace <span class="c-primary">People</span></h1>
        </div>
      </div>
    </div>
    <section class="work-detail">
      <div class="container">
        <div class="work-detail-image"></div>
        <div class="work-detail__slider">
          <div ref="workSlider" class="swiper">
            <div class="swiper-wrapper">
              <div class="swiper-slide">
                <div class="work-detail__slider-item">
                  <img src="~/static/images/chace-slider-img-1.jpg" alt="" />
                </div>
              </div>
              <div class="swiper-slide">
                <div class="work-detail__slider-item">
                  <img src="~/static/images/chace-slider-img-2.jpg" alt="" />
                </div>
              </div>
              <div class="swiper-slide">
                <div class="work-detail__slider-item">
                  <img src="~/static/images/chace-slider-img-3.jpg" alt="" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div class="work-detail__about">
          <h2 class="txt txt--rem48 txt--font300 c-white text-center">
            About Chace <b>People</b>
          </h2>
          <br />
          <p class="txt txt--rem32 txt--font300 c-white text-center">
            Chace People is a leading specialist recruitment agency, placing
            senior support staff with high profile clients around the world.
            They connect and they match, creating the three cs of Chace; client,
            consultant and candidate. Chace people works on a project basis
            whereby our teams connect with the best candidates, creating
            opportunities for our clients to work with the most respected talent
            within their specific industries. with the use of technology and our
            in-depth interview and vetting process, we work closely with our
            clients and candidates to ensure that we match the right people with
            the right people.
          </p>
          <br />
          <br />
          <a href="https://chacepeople.com" target="_blank">
            <v-button
              color=""
              icon="iconArrow"
              hover="primary"
              text="Visit Website"
              type="centered"
            />
          </a>
        </div>
      </div>
    </section>
    <section class="work-detail__info">
      <div class="container">
        <div class="row g-4 g-md-5">
          <div class="col-12 col-md-6 col-lg-4 col-xl-3">
            <div class="work-detail__info-card">
              <div
                class="work-detail__info-card__title txt txt--rem48 txt--font400 c-white"
              >
                Chace People
              </div>
              <div
                class="work-detail__info-card__value txt txt--rem32 txt--font300 c-white"
              >
                Client
              </div>
            </div>
          </div>
          <div class="col-12 col-md-6 col-lg-4 col-xl-3">
            <div class="work-detail__info-card">
              <div
                class="work-detail__info-card__title txt txt--rem48 txt--font400 c-white"
              >
                UK, England
              </div>
              <div
                class="work-detail__info-card__value txt txt--rem32 txt--font300 c-white"
              >
                Country
              </div>
            </div>
          </div>
          <div class="col-12 col-md-6 col-lg-4 col-xl-3">
            <div class="work-detail__info-card">
              <div
                class="work-detail__info-card__title txt txt--rem48 txt--font400 c-white"
              >
                Corporate
              </div>
              <div
                class="work-detail__info-card__value txt txt--rem32 txt--font300 c-white"
              >
                Type
              </div>
            </div>
          </div>
          <div class="col-12 col-md-6 col-lg-4 col-xl-3">
            <div class="work-detail__info-card">
              <div
                class="work-detail__info-card__title txt txt--rem48 txt--font400 c-white"
              >
                2 Months
              </div>
              <div
                class="work-detail__info-card__value txt txt--rem32 txt--font300 c-white"
              >
                Duration
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div class="work-detail__gallery">
          <div class="work-detail__gallery-item">
            <img src="~/static/images/chace-gallery-1.png" alt="" />
          </div>
          <div class="work-detail__gallery-item">
            <img src="~/static/images/chace-gallery-2.png" alt="" />
          </div>
          <div class="work-detail__gallery-item">
            <img src="~/static/images/chace-gallery-3.png" alt="" />
          </div>
          <div class="work-detail__gallery-item">
            <img src="~/static/images/chace-gallery-4.png" alt="" />
          </div>
          <div class="work-detail__gallery-item">
            <img src="~/static/images/chace-gallery-5.png" alt="" />
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <h2 class="txt txt--rem48 txt--font300 c-white text-center">
          Do you want to same <b>Website?</b>
        </h2>
        <br />
        <p class="txt txt--rem32 txt--font300 c-white text-center">
          If you like this website, you can get the offer below and have the
          most special website designed for you. Contact us now and let's bring
          your dream website to the
          <span class="color: var(--c-primary)">real world!</span>
        </p>
        <br />
        <br />
        <nuxtLink to="/contact">
          <v-button
            color=""
            icon="iconArrow"
            hover="primary"
            text="Get an Offer"
            type="centered"
          />
        </nuxtLink>
      </div>
    </section>
  </main>
</template>

<script>
import { Swiper, Autoplay } from "swiper";
Swiper.use([Autoplay]);
export default {
  data() {
    return {
      // workDetail: [],
      routeId: this.$route.params.workDetail,
    };
  },
  mounted() {
    // const result = this.$store.state.workList.filter((obj) => {
    //   return obj.title.toLowerCase().replace(/ /g, "-") === this.routeId;
    // });
    // this.workDetail = result[0];
    const workSlider = new Swiper(this.$refs.workSlider, {
      loop: true,
      slidesPerView: 3,
      spaceBetween: 40,
      speed: 1500,
      autoplay: {
        delay: 3000,
      },
      breakpoints: {
        320: { slidesPerView: 1 },
        569: { slidesPerView: 2 },
        991: { slidesPerView: 3 },
      },
    });
  },
};
</script>
