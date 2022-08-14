<template>
  <section class="mainSection">
    <div class="content">
      <p class="text">
        Hello there, my name is <span class="name">Salma</span>
      </p>
      <p class="sassy_text">I build things for the WEB</p>
      <p class="text">
        I build Scalable frontend applications with great user experience
      </p>
      <div class="btn__wrapper">
        <button class="btn">
          <NuxtLink to="/contactMe">Get In Touch With Me</NuxtLink>
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MainSection',
}
</script>

<style scoped>
.mainSection {
  width: 90%;
  /* height: 450px; */
  color: white;
  display: grid;
  grid-gap: 10px;
  padding: 0 10px;
  margin: 70px auto 0;
  /* border: 1px solid red; */
}
.image {
  width: 100%;
  height: 100%;
}
.content p {
  text-align: center;
}
.btn {
  max-width: 200px;
  height: 54px;
  background: #4284ff;
  border-radius: 10px;
  font-family: 'Inter';
  font-weight: 400;
  font-size: 14px;
  line-height: 24px;
  color: #ffffff;
  border: none;
  cursor: pointer;
  margin-top: 24px;
  padding: 0 20px;
}
a {
  color: #ffffff;
}
.btn__wrapper {
  display: flex;
  justify-content: center;
}
.btn:hover {
  background: #c4d8fe;
  color: #4284ff;
}
.avatar {
  width: 95%;
  height: 100%;
}
.text {
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 36px;
}
.sassy_text {
  font-style: normal;
  font-weight: 400;
  font-size: 28px;
  line-height: 44px;
  background: radial-gradient(50% 50% at 50% 50%, #4254ff 0%, #c4d8fe 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.name {
  font-style: normal;
  font-weight: 400;
  font-size: 64px;
  line-height: 96px;
}

@media screen and (min-width: 768px) {
  .mainSection {
    padding: 0 30px;
    max-width: 100%;
    width: 80%;
  }
  .text {
    font-style: normal;
    font-weight: 400;
    font-size: 36px;
    line-height: 54px;
  }
  .name {
    font-style: normal;
    font-weight: 400;
    font-size: 64px;
    line-height: 96px;
  }
  .sassy_text {
    font-size: 64px;
    line-height: 96px;
  }
  .content {
    /* display: grid; */
    /* place-content: center; */
    max-width: 865px;
  }
  .content p {
    text-align: left;
  }
  .btn {
    max-width: 240px;
    font-weight: 400;
    font-size: 18px;
    line-height: 29px;
  }
  .btn__wrapper {
    justify-content: start;
  }
}
</style>