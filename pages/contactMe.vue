<template>
  <Layout>
    <div class="contact">
      <div class="contact-body">
        <img src="@/assets/avt.png" alt="" />
      </div>
      <div class="contact-text">
        <p>
          Want to bring your amazing ideas to life? Lets get together to make
          fun, interactive things with code.
        </p>
        <p>Email me: salma@enyata.com</p>
      </div>
    </div>
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
.contact {
  display: flex;
  flex-direction: column;
  width: 80%;
  margin: auto;
  align-items: center;
  padding-top: 30px;
  gap: 50px;
  /* min-height: 110vh; */
}
.contact-body {
  width: 250px;
  height: 250px;
  border-radius: 50%;
  background-color: #98bcfe;
  display: flex;
  align-items: center;
  justify-content: center;
}
.contact-body img {
  width: 220px;
}
.contact-text {
  max-width: 700px;
  text-align: center;
}
.contact-text p {
  font-weight: 500;
  font-size: 32px;
  line-height: 52px;
  color: #98bcfe;
}
@media screen and (min-width: 768px) {
  .contact {
    height: calc(100vh - 120px);
    grid-template-columns: 30vw 1fr;
  }
  .contact-body {
    width: 320px;
    height: 320px;
    border-radius: 50%;
    background-color: #98bcfe;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .contact-body img {
    width: 250px;
  }
}
</style>