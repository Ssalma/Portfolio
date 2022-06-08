<template>
  <section class="mainSection">
    <div class="content">
      <p class="text">
        Hello there, my name is <span class="name">Salma</span>
      </p>
      <p class="sassy_text">I biuld things for the WEB</p>
      <p class="text">
        I build Scalable frontend applications with great user experience
      </p>
      <div class="btn__wrapper">
        <button class="btn">Get In Touch With Me</button>
      </div>
    </div>
    <div class="overhead">
      <!-- <img src="@/assets/vue.svg" alt="" class="image"> -->
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style>

.mainSection {
  width: 86%;
  height: 450px;
  color: white;
  display: grid;
  grid-gap: 10px;
  padding: 0 10px;
  margin: auto;
}
.overhead {
  max-width: 380px;
  height: 360px;
  margin: auto;
}
.image{
  width: 100%;
  height: 100%;
}
.content {
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
  font-size: 16px;
  line-height: 28px;
}
.sassy_text {
  font-style: normal;
  font-weight: 400;
  font-size: 28px;
  line-height: 44px;
  background: linear-gradient(180deg, #4284ff 0%, #c4d8fe 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.name {
  font-style: normal;
  font-weight: 400;
  font-size: 28px;
  line-height: 38px;
}
@media screen and (min-width: 768px) {
  .mainSection {
    grid-template-columns: repeat(2, minmax(350px, max-content));
    justify-content: space-between;
    padding: 0 30px;
    max-width: 100%;
  }
  .text {
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 26px;
  }
  .name {
    font-style: normal;
    font-weight: 400;
    font-size: 48px;
    line-height: 70px;
  }
  .sassy_text {
    font-size: 54px;
    line-height: 80px;
  }
  .content {
    display: grid;
    place-content: center;
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