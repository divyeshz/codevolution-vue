<template>
  <div>
    {{ greet }} {{ name }}
  </div>
  <div v-html="channel"></div>
  <div v-html="hack"></div>
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Bind</button>
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
      headingId: 'heading',
      isDisabled: false,
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
