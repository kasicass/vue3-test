<script>
import Header from './Header.vue'
import Main from './Main.vue'
import Footer from './Footer.vue'

export default {
  components: {
    Header,
    Main,
    Footer,
  },
}
</script>

<template>
  <Header></Header>
  <Main></Main>
  <Footer></Footer>
</template>

<style scoped>
.header,
.main,
.footer {
  border: 1px solid #999;
  margin-bottom: 4px;
}
</style>
