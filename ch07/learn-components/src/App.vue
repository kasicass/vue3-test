<script>
import Header from './Header.vue'
import Main from './Main.vue'
import Footer from './Footer.vue'
import NoPropAttribute from './NoPropAttribute.vue'
import CounterOperation from './CounterOperation.vue'

export default {
  components: {
    Header,
    Main,
    Footer,
    NoPropAttribute,
    CounterOperation,
  },
  data() {
    return {
      counter: 0,
    }
  },
  methods: {
    addOne() {
      this.counter++
    },
    subOne() {
      this.counter--
    },
    addNNum(num, name, age) {
      console.log(name, age)
      this.counter += num
    },
  },
}
</script>

<template>
  <Header></Header>
  <Main></Main>
  <Footer></Footer>
  <NoPropAttribute class="why" id="coder" name="phay"></NoPropAttribute>
  <div>
    <h4>当前计数：{{ counter }}</h4>
    <CounterOperation @add="addOne" @sub="subOne" @addN="addNNum"></CounterOperation>
  </div>
</template>

<style scoped>
.header,
.main,
.footer {
  border: 1px solid #999;
  margin-bottom: 4px;
}
</style>
