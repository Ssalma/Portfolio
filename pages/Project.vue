<template>
  <Layout show-avataar>
    <section class="sectionPage">
      <h2 class="header">PROJECTS</h2>
      <section class="projects__wrapper">
        <div class="project">
          <div class="project__content">
            <div class="image__wrapper">
              <img class="image" src="@/assets/instrail.png" alt="" />
            </div>
            <div class="content">
              <a href="https://instrail.enyata.com/" target="_blank">
                <h3 class="title">Instrail</h3>
              </a>
              <ul>
                <li class="description">An insurance management plaform</li>
                <li class="description">
                  <span> Project type </span>: Corporate, Insurance, Dashboard.
                </li>
                <li class="description">
                  <span> Tech Stack </span> : Vue, Vuex, Html, Css
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="project">
          <div class="project__content">
            <div class="image__wrapper">
              <img class="image" src="@/assets/kwerty.png" alt="" />
            </div>
            <div class="content">
              <a href="https://kwerty.io/" target="_blank">
                <h3 class="title">Kwerty</h3>
              </a>
              <ul>
                <li class="description">Public data engine platform</li>
                <li class="description">
                  <span> Project type </span>: marketing, search Website..
                </li>
                <li class="description">
                  <span> Tech Stack </span> : Vue, Vuex, Html, Css, chartJs
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="project">
          <div class="project__content">
            <div class="image__wrapper">
              <img class="image" src="@/assets/comment.png" alt="" />
            </div>
            <div class="content">
              <a href="https://chatcomment-app.netlify.app/" target="_blank">
                <h3 class="title">Interactive comment section</h3>
              </a>
              <ul>
                <li class="description">Single user comment section</li>
                <li class="description">
                  <span> Project type </span>: Comment app
                </li>
                <li class="description">
                  <span> Tech Stack </span> : Vue, Vuex, Javascript, Firebase
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>
    </section>
  </Layout>
</template>

<script>
import Layout from '@/components/Layout.vue'
export default {
  name: 'ProjectsPage',
  components: {
    Layout,
  },
  // transition: {
  //   name: 'scale',
  //   mode: 'out-in',
  //   css: false,

  //   beforeEnter(el) {
  //     this.$gsap.set(el, {
  //       opacity: 0.5,
  //       scale: 0,
  //     })
  //   },

  //   enter(el, done) {
  //     this.$gsap.to(el, {
  //       opacity: 1,
  //       scale: 1,
  //       duration: 1,
  //       ease: 'power2.inOut',
  //       onComplete: done,
  //     })
  //   },

  //   leave(el, done) {
  //     this.$gsap.to(el, {
  //       opacity: 0,
  //       scale: 0,
  //       duration: 1,
  //       ease: 'power2.inOut',
  //       onComplete: done,
  //     })
  //   },
  // },
}
</script>
<style scoped>
.sectionPage {
  width: 96%;
  margin: auto;
  background: #161b22;
  padding: 10px 0 50px;
  height: auto;
}
.projects__wrapper {
  overflow: auto;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 20px;
  padding: 20px 10px;
}
.header {
  font-weight: 700;
  font-size: 32px;
  line-height: 39px;
  color: #ffffff;
  text-align: center;
}
.image__wrapper img {
  width: 100%;
}
.project {
  width: 100%;
  max-width: 400px;
  height: auto;
  background: #c4d8fe;
  /* background: #5222d0; */
  border-radius: 5px;
  margin: auto;
  padding: 26px 10px;
}
.project__content {
  width: 85%;
  margin: auto;
}
.title {
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 36px;
  color: #4284ff;
}
.description {
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 27px;
  color: #000000;
  /* color: #fff; */
}
@media screen and (min-width: 768px) {
  .sectionPage {
    width: 80%;
    padding: 20px 0;
  }
  .projects__wrapper {
    grid-template-columns: repeat(auto-fill, minmax(490px, max-content));
    grid-gap: 50px;
    place-content: center;
    width: 100%;
  }
  .project {
    width: 100%;
    max-width: 490px;
    height: 580px;
  }
}
</style>
