<template>
  <main class="mainPage">
    <section class="main__section">
      <NavBar></NavBar>
      <!-- <div class="circle"></div> -->
      <section class="">
        <slot />
      </section>
    </section>
  </main>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
<style scoped>
/* .circle {
  width: 500px;
  height: 500px;
  border-radius: 50%;
  background-color: #c4d8fe;
  position: absolute;
  /* right: -10vw; */
  /* top: -50px; */
  /* transform: translateX(210%);
} */
.mainPage {
  width: 100%;
  height: auto;
  padding: 10px;
  background: linear-gradient(180deg, #4284ff 0%, #c4d8fe 100%);
  box-sizing: border-box;
}
.main__section {
  width: 100%;
  height: auto;
  min-height: 120vh;
  margin: auto;
  background: #161b22;
}
main {
  background-color: #161b22;
}

@media screen and (min-width: 768px) {
  .mainPage {
    height: auto;
  }
  .main__section {
    min-height: calc(100vh - 20px);
  }
}
</style>
