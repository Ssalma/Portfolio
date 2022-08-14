<template>
  <main class="mainPage">
    <div class="social__icons">
      <a href="https://linkedin.com/in/salma-salihu" target="_blank">
        <img src="@/assets/linkedIn.svg" alt="" />
      </a>
      <a href="https://github.com/Ssalma" target="_blank">
        <img src="@/assets/github.svg" alt="" />
      </a>
      <a href="https://twitter.com/Mahyasalisalma" target="_blank">
        <img src="@/assets/twitter.svg" alt="" />
      </a>
    </div>
    <div v-if="showAvataar" class="avataar_wrapper">
      <img src="@/assets/avt.png" alt="" />
    </div>
    <section class="main__section">
      <NavBar></NavBar>
      <section class="section1">
        <slot />
      </section>
    </section>
  </main>
</template>

<script>
export default {
  name: 'IndexPage',
  props: {
    showAvataar: {
      type: Boolean,
    },
  },
  mounted() {
    this.staggering()
  },
  methods: {
    staggering() {
      const gsap = this.$gsap
      gsap.from('.avataar_wrapper', {
        x: -200,
        opacity: 0.2,
        stagger: 0.5,
        duration: 1.8,
        // repeat: Infinity,
      })
    },
  },
}
</script>
<style scoped>
.avataar_wrapper {
  width: 250px;
  height: 250px;
  position: absolute;
  bottom: 20px;
  right: 0px;
  display: none;
}
.avataar_wrapper img {
  width: 100%;
}
.mainPage {
  width: 100%;
  background: linear-gradient(180deg, #4284ff 0%, #c4d8fe 100%);
  box-sizing: border-box;
  position: relative;
  height: 100vh;
}
.main__section {
  width: 100%;
  height: 100vh;
  margin: auto;
  background: #161b22;
  overflow: auto;
}
main {
  background-color: #161b22;
}
.social__icons {
  position: absolute;
  bottom: 20px;
  transform: translateX(-50%);
  left: 50%;
  display: flex;
  grid-gap: 20px;
}
.social__icons img {
  cursor: pointer;
}
.section1::before {
  display: none;
}
@media screen and (min-width: 768px) {
  .mainPage {
    height: auto;
  }
  .main__section {
    min-height: calc(100vh - 12px);
  }
  .avataar_wrapper {
    display: flex;
  }
  .section1::before {
    display: block;
    content: '';
    position: absolute;
    top: 100px;
    left: 70px;
    border: 1px solid #4284ff;
    min-height: 55vh;
    height: auto;
    z-index: 10;
    background: linear-gradient(to right, #4284ff, #4284ff);
  }
  .social__icons {
    position: absolute;
    top: 80vh;
    left: 70px;
    display: grid;
    grid-gap: 20px;
  }
  .social__icons img {
    cursor: pointer;
  }
}
</style>
