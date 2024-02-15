<template>
  <h2>{{ name }}</h2>
  <div>
    <button @click="name = 'Neel'">Change Name!</button>
    <button @mouseover="name = 'Neel'">Change Name!</button>
  </div>

  <h2>{{ count }}</h2>
  <div>
    <button @click="count++">Increment</button>
    <button @click="count--">Decrement</button>
  </div>
  <hr>
  <div>
    <button @click="increment(1)">Method Increment 1</button>
    <button @click="increment(5)">Method Increment 5</button>
    <button @click="decrement(2)">Method Decrement 2</button>
    <button @click="decrement(5)">Method Decrement 5</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'Divyesh',
      count: 0,
    }
  },
  methods: {
    changeName() {
      this.name = 'Neel'
    },
    increment(num) {
      this.count += num
    },
    decrement(num) {
      this.count -= num
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
