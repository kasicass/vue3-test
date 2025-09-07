<script>
import Header from './Header.vue'
import Main from './Main.vue'
import Footer from './Footer.vue'
import NoPropAttribute from './NoPropAttribute.vue'

export default {
  components: {
    Header,
    Main,
    Footer,
    NoPropAttribute,
  },
}
</script>

<template>
  <Header></Header>
  <Main></Main>
  <Footer></Footer>
  <NoPropAttribute class="why" id="coder" name="phay"></NoPropAttribute>
</template>

<style scoped>
.header,
.main,
.footer {
  border: 1px solid #999;
  margin-bottom: 4px;
}
</style>
