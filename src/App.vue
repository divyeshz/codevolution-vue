<template>
  <div>
    {{ greet }} {{ name }}
  </div>
  <div v-html="channel"></div>
  <div v-html="hack"></div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: "Divyesh",
      greet: "Hello",
      channel: '<b>Divyesh Youtube</b>',
      hack: `<a href="#" onclick="alert('hacked!')">Win a prize!</a>`,
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
