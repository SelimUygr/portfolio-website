<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-wrapper">
        <div class="footer__info row">
          <div class="col-12 col-lg-3">
            <div class="footer__info-logo">
              <img src="~/static/images/buffalo-logo.svg" alt="" />
            </div>
          </div>
          <div class="col-12 col-lg-9">
            <div class="footer__info-content">
              <div
                v-for="(item, index) in profiles[0]?.items"
                :key="index"
                class="footer__info-content__item"
              >
                <div
                  class="footer__info-content__item-title txt txt--rem28 txt--font300 c-paragraph"
                >
                  {{ item.title }}
                </div>
                <div
                  class="footer__info-content__item-text txt txt--rem28 txt--font900 c-white"
                >
                  {{ item.text }}
                </div>
                <div
                  v-if="item.socials"
                  class="footer__info-content__item-socials"
                >
                  <div
                    v-for="(social, index) in item.socials"
                    :key="index"
                    class="footer__info-content__item-socials__item"
                  >
                    <a target="_blank" :href="social.link">
                      <svg-icon :name="social.icon" />
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer__rights">
      <div class="container">
        <div class="footer__rights-text txt txt--rem24 txt--font300">
          ALL RIGHTS RESERVED BY <span>SELIM</span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      profiles: [
        {
          items: [
            {
              text: "omsuygur@gmail.com",
              title: "mail",
            },
            {
              text: "Bursa / Nilüfer",
              title: "address",
            },
            {
              text: "0 542 608 07 98",
              title: "Phone",
            },
            {
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
              title: "socials",
            },
          ],
          name: "Ömer Selim Uygur",
        },
      ],
    };
  },
};
</script>
