<template>
  <Layout>
    <section class="sectionPage">
      <h2 class="header">PROJECTS</h2>
      <section class="projects__wrapper">
        <div class="project">
          <div class="project__content">
            <div class="image__wrapper">
              <img class="image" src="@/assets/instrail.png" alt="" />
            </div>
            <div class="content">
              <h3 class="title">Instrail</h3>
              <ul>
                <li class="description">An insurance management plaform</li>
                <li class="description">
                  <span> Project type </span>: Corporate, Insurance, Dashboard.
                </li>
                <li class="description"> <span> Tech Stack </span> : Vue, Vuex, Html, Css</li>
              </ul>
            </div>
          </div>
        </div>
        <div class="project"></div>
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
}
</script>
<style scoped>
.sectionPage {
  width: 100%;
  background: #161b22;
}
.projects__wrapper {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 20px;
  padding: 0 10px;
}
.header {
  font-family: 'Inter';
  font-weight: 700;
  font-size: 32px;
  line-height: 39px;
  color: #ffffff;
  text-align: center;
}
.project {
  width: 100%;
  max-width: 400px;
  height: 580px;
  background: #c4d8fe;
  border-radius: 5px;
  margin: auto;
  padding: 26px 10px;
}
.project__content {
  width: 85%;
  margin: auto;
}
.title {
  font-family: 'Poppins';
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 36px;
  color: #4284ff;
}
.description {
  font-family: 'Poppins';
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 27px;

  color: #000000;
}
@media screen and (min-width: 768px) {
  .projects__wrapper {
    grid-template-columns: repeat(auto-fill, minmax(490px, max-content));
    grid-gap: 50px;
    place-content: center;
    width: 100%;
  }
  .project {
    width: 100%;
    max-width: 490px;
  }
}
</style>
