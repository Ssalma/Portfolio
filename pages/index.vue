<template>
  <Layout>
    <conTent></conTent>
  </Layout>
</template>

<script>
import conTent from '@/components/conTent.vue';
import Layout from '@/components/Layout.vue';
export default {
  name: 'IndexPage',
  components: {
    Layout,
    conTent,
  },
}
</script>
<style scoped>
</style>
