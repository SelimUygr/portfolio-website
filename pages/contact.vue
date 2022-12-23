<template>
  <main class="detail-page">
    <div class="container">
      <div class="subheader">
        <div class="subheader__title txt txt--rem128 txt--font900 c-white">
          <h1>Contact <span class="c-primary">Us</span></h1>
        </div>
      </div>
    </div>
    <section>
      <div class="container">
        <div class="contact__info row g-4 g-md-5">
          <div class="col-12 col-lg-4">
            <div class="about__image">
              <img src="~/static/images/oms-img.png" alt="" />
            </div>
          </div>
          <div class="col-12 col-lg-8">
            <div class="about__info c-white">
              <div class="txt txt--rem48 txt--font300">Ömer Selim Uygur</div>
              <div class="txt txt--rem24 txt--font300 c-paragraph">
                Software Developer
              </div>
              <div class="contact__info-cards mt-5">
                <div class="contact__info-cards__item">
                  <div
                    class="contact__info-cards__item-title txt txt--rem28 txt--font300 c-primary"
                  >
                    mail
                  </div>
                  <div
                    class="contact__info-cards__item-subtitle txt txt--rem32 txt--font700 c-white"
                  >
                    omsuygur@gmail.com
                  </div>
                </div>
                <div class="contact__info-cards__item">
                  <div
                    class="contact__info-cards__item-title txt txt--rem28 txt--font300 c-primary"
                  >
                    address
                  </div>
                  <div
                    class="contact__info-cards__item-subtitle txt txt--rem32 txt--font700 c-white"
                  >
                    Bursa / Nilüfer
                  </div>
                </div>
                <div class="contact__info-cards__item">
                  <div
                    class="contact__info-cards__item-title txt txt--rem28 txt--font300 c-primary"
                  >
                    socials
                  </div>
                  <div
                    class="contact__info-cards__item-subtitle txt txt--rem32 txt--font700 c-white"
                  >
                    <div
                      v-if="socials"
                      class="footer__info-content__item-socials justify-content-start"
                    >
                      <div
                        v-for="(social, index) in socials"
                        :key="index"
                        class="footer__info-content__item-socials__item me-5"
                      >
                        <a target="_blank" :href="social.link">
                          <svg-icon :name="social.icon" />
                        </a>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="contact__info-cards__item">
                  <div
                    class="contact__info-cards__item-title txt txt--rem28 txt--font300 c-primary"
                  >
                    phone
                  </div>
                  <div
                    class="contact__info-cards__item-subtitle txt txt--rem32 txt--font700 c-white"
                  >
                    0 542 608 07 98
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div class="contact-form">
          <h2 class="txt txt--rem48 txt--font300 c-white text-center mb-5">
            Tell me about your Dream <b>Website</b>
          </h2>
          <div class="row g-4 g-md-5">
            <div class="col-12 col-lg-6">
              <div class="input-item">
                <input type="text" placeholder="Name Surname" />
              </div>
            </div>
            <div class="col-12 col-lg-6">
              <div class="input-item">
                <input type="text" placeholder="Company Name" />
              </div>
            </div>
            <div class="col-12 col-lg-6">
              <div class="input-item">
                <input type="text" placeholder="Phone" />
              </div>
            </div>
            <div class="col-12 col-lg-6">
              <div class="input-item">
                <input type="text" placeholder="Name Surname" />
              </div>
            </div>
            <div class="col-12">
              <div class="input-item input-item--textarea">
                <textarea name="" cols="30" rows="10" placeholder="Message">
                </textarea>
              </div>
            </div>
            <div class="col-12">
              <v-button
                color=""
                icon="iconArrow"
                hover="primary"
                text="submit"
                type="centered"
              />
            </div>
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
      socials: [
        {
          icon: "iconLinkedin",
          link: "https://www.linkedin.com/in/omer-selim-uygur-233387188",
        },
        {
          icon: "iconGithub",
          link: "https://github.com/SelimUygr",
        },
        {
          icon: "iconInstagram",
          link: "https://www.instagram.com/selimygr/",
        },
      ],
    };
  },
};
</script>
