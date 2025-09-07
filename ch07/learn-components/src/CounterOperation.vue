<template>
  <div>
    <button @click="increment">+1</button>
    <button @click="decrement">-1</button>
    <input type="text" v-model.number="num"></input>
    <button @click="incrementN">+n</button>
  </div>
</template>

<script>
export default {
  // emits: ['add', 'sub', 'addN'],
  emits: {
    add: null,
    sub: null,
    addN: (num, name, age) => {
        if (num > 10) {
            return true
        }

        return false
    }
  },
  data() {
    return {
        num: 0
    }
  },
  methods: {
    increment() {
      this.$emit('add')
    },
    decrement() {
      this.$emit('sub')
    },
    incrementN() {
        this.$emit('addN', this.num, "why", 18)
    }
  },
}
</script>
