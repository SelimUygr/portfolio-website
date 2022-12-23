<template>
  <main class="detail-page">
    <div class="container">
      <div class="subheader">
        <div class="subheader__title txt txt--rem128 txt--font900 c-white">
          <h1>About <span class="c-primary">Me</span></h1>
        </div>
      </div>
      <div class="about__wrapper row g-4 g-md-5">
        <div class="col-12 col-lg-4">
          <div class="about__sticky">
            <div class="about__image">
              <img src="~/static/images/oms-img.png" alt="" />
            </div>
            <div class="about__info c-white mt-5">
              <div class="txt txt--rem48 txt--font300">
                Ömer Selim <b>Uygur</b>
              </div>
              <div class="txt txt--rem24 txt--font300 c-paragraph">
                Software Developer
              </div>
              <div class="about__info-cards mt-5">
                <div class="about__info-cards__item">
                  <div
                    class="about__info-cards__item-title txt txt--rem28 txt--font300 c-primary"
                  >
                    mail
                  </div>
                  <div
                    class="about__info-cards__item-subtitle txt txt--rem32 txt--font700 c-white"
                  >
                    omsuygur@gmail.com
                  </div>
                </div>
                <div class="about__info-cards__item">
                  <div
                    class="about__info-cards__item-title txt txt--rem28 txt--font300 c-primary"
                  >
                    address
                  </div>
                  <div
                    class="about__info-cards__item-subtitle txt txt--rem32 txt--font700 c-white"
                  >
                    Bursa / Nilüfer
                  </div>
                </div>
                <div class="about__info-cards__item">
                  <div
                    class="about__info-cards__item-title txt txt--rem28 txt--font300 c-primary"
                  >
                    socials
                  </div>
                  <div
                    class="about__info-cards__item-subtitle txt txt--rem32 txt--font700 c-white"
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
                <div class="about__info-cards__item">
                  <div
                    class="about__info-cards__item-title txt txt--rem28 txt--font300 c-primary"
                  >
                    phone
                  </div>
                  <div
                    class="about__info-cards__item-subtitle txt txt--rem32 txt--font700 c-white"
                  >
                    0 542 608 07 98
                  </div>
                </div>
              </div>
              <div class="about__info-languages mt-5">
                <div class="about__info-languages__item">
                  Turkish <span>Native</span>
                </div>
                <div class="about__info-languages__item">
                  Chinese <span>Fluent</span>
                </div>
                <div class="about__info-languages__item">
                  English <span>Fluent</span>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 col-lg-8">
          <div class="about__content">
            <h1 class="txt txt--rem48 txt--font300 c-white mb-5">
              About <span class="txt--font400">Me</span>
            </h1>
            <div
              class="about__content__text txt txt--rem32 txt--font300 c-white"
            >
              I am a <span>Software Engineer</span> who has been keeping up with
              the developing technologies for <span>almost 5 years</span>, not
              afraid to experiment, and has been
              <span>developing quality softwares</span> in this process. With my
              results-oriented mindset, I have ensured unequivocal satisfaction
              with the product or service by searching, learning and applying
              efficient technologies. While developing quality projects, I
              always <span>aimed my vision at the top</span> and used the most
              appropriate technology for the projects. I am
              <span>experienced in working with a team and</span> I see myself
              as someone who can contribute to teamwork.
              <span> my vision; is to improve myself</span> and where I am to
              always be the best you can be.
            </div>
          </div>
          <div class="about__education">
            <h1 class="txt txt--rem48 txt--font300 c-white mb-5">
              Education <span class="txt--font400">Phase</span>
            </h1>
            <div class="about__education__wrapper">
              <div class="about__education-item d-flex align-items-center">
                <div
                  class="about__education-item__date txt txt--rem32 txt--font700 c-white"
                >
                  2023-2018
                </div>
                <div class="about__education-item__content">
                  <div class="txt txt--rem32 txt--font700 c-white">
                    <p>BACHELORS DEGREE</p>
                    <span class="txt txt--rem24 txt--font400 c-paragraph">
                      Beijing Information Science & Technology University
                    </span>
                  </div>
                </div>
              </div>
              <div class="about__education-item d-flex align-items-center">
                <div
                  class="about__education-item__date txt txt--rem32 txt--font700 c-white"
                >
                  2016-2012
                </div>
                <div class="about__education-item__content">
                  <div class="txt txt--rem32 txt--font700 c-white">
                    <p>HIGH SCHOOL GRADUATE</p>
                    <span class="txt txt--rem24 txt--font400 c-paragraph">
                      Final Okulları
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="about__skills">
            <div class="index-about__skills-progress p-0" v-if="skills">
              <div
                v-for="(item, index) in skills"
                :key="index"
                class="index-about__skills-progress__item"
              >
                <div class="index-about__skills-progress__item-title">
                  <h4 class="txt txt--rem32 txt--font400 c-white">
                    {{ item.title }}
                  </h4>
                </div>
                <div class="index-about__skills-progress__item-line progress">
                  <div
                    class="progress-bar"
                    ref="progressItem"
                    role="progressbar"
                    :style="'width:' + item.percent + '%'"
                    aria-valuenow="0"
                    aria-valuemin="0"
                    aria-valuemax="100"
                  ></div>
                </div>
              </div>
            </div>
          </div>
          <div class="about__experience">
            <h1 class="txt txt--rem48 txt--font300 c-white mb-5">
              Work <span class="txt--font400">Experience</span>
            </h1>
            <div class="about__education__wrapper">
              <div class="about__education-item d-flex align-items-center">
                <div
                  class="about__education-item__date txt txt--rem32 txt--font700 c-white"
                >
                  Now-2022
                </div>
                <div class="about__education-item__content">
                  <div class="txt txt--rem32 txt--font700 c-white">
                    BABEL AGENCY
                    <br />
                    <span class="txt txt--rem24 txt--font400 c-paragraph">
                      Full Stack Developer
                    </span>
                  </div>
                </div>
              </div>
              <div class="about__education-item d-flex align-items-center">
                <div
                  class="about__education-item__date txt txt--rem32 txt--font700 c-white"
                >
                  2022-2019
                </div>
                <div class="about__education-item__content">
                  <div class="txt txt--rem32 txt--font700 c-white">
                    Dimassi Furnitures
                    <br />
                    <span class="txt txt--rem24 txt--font400 c-paragraph">
                      Translator, Software System Designer/Developer,
                      Production, Coordination Project Manager
                    </span>
                  </div>
                </div>
              </div>
              <div class="about__education-item d-flex align-items-center">
                <div
                  class="about__education-item__date txt txt--rem32 txt--font700 c-white"
                >
                  2018-2017
                </div>
                <div class="about__education-item__content">
                  <div class="txt txt--rem32 txt--font700 c-white">
                    The Bell X Terezza Martini
                    <br />
                    <span class="txt txt--rem24 txt--font400 c-paragraph">
                      Waiter, Supervisor
                    </span>
                  </div>
                </div>
              </div>
              <div class="about__education-item d-flex align-items-center">
                <div
                  class="about__education-item__date txt txt--rem32 txt--font700 c-white"
                >
                  2017-2016
                </div>
                <div class="about__education-item__content">
                  <div class="txt txt--rem32 txt--font700 c-white">
                    English Tutor
                    <br />
                    <span class="txt txt--rem24 txt--font400 c-paragraph">
                      Kindergarten in China/Beijing
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);
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
      skills: [
        { title: "Phyton", percent: 76 },
        { title: "Java", percent: 66 },
        { title: "Kivy", percent: 57 },
        { title: "Php", percent: 37 },
        { title: "C", percent: 70 },
      ],
    };
  },
  mounted() {
    gsap.from(this.$refs.progressItem, {
      scrollTrigger: {
        trigger: this.$refs.progressItem,
        start: "center-=100 center",
        end: "center-=100 center",
      },
      width: 0,
      ease: "power2",
      duration: 1,
    });
  },
};
</script>
