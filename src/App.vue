<template>
  <h2>Volume Tracker (0-20)</h2>
  <h3>Current Volume - {{ volume }}</h3>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>

  <input type="text" v-model="movie" name="" id="">
  <input type="text" v-model="movieInfo.title" name="" id="">
  <input type="text" v-model="movieInfo.actor" name="" id="">

  <div>
    <button @click="movieList = movieList.concat(['Wonder Women'])">Add Movie</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      volume: 0,
      movie: 'Batman',
      movieInfo: {
        title: '',
        actor: ''
      },
      movieList: [
        'Batman', 'Superman'
      ]
    }
  },
  methods: {
  },
  computed: {
  },
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert('damage');
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Call Api with movie name = ${newValue}  `);
      },
      immediate: true,
    },
    movieInfo: {
      handler(newValue) {
        console.log(`Call Api with movie title = ${newValue.title} and actor = ${newValue.actor}`);
      },
      deep: true,
    },
    movieList: {
      handler(newValue) {
        console.log(`Updated list ${newValue}`);
      },
      // deep: true,
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
