<template>
  <h2 v-if="num === 0">The Number is zero</h2>
  <h2 v-else-if="num < 0">The Number is negative</h2>
  <h2 v-else-if="num > 0">The Number is positive</h2>
  <h2 v-else>The Number is Not a number</h2>

  <template v-if="display">
    <h2>Divyesh</h2>
    <h2>Youtube</h2>
    <h2>Vue 3</h2>
  </template>

  <h2 v-show="showElement">Using v-show</h2>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      num: 12,
      display: true,
      showElement: false,

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
