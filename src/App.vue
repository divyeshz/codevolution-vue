<template>
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Bind</button>
  <h2 class="underline">
    This is my first Vue 3 code
  </h2>
  <h2 class="underline" :class="status">status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldOut ? 'sold-out' : 'new'">SoldOut? Movie</h2>
  <h2 :class="['new', 'promoted']">New Promoted Movie</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">Array Conditional Movie</h2>
  <h2 :class="{
    promoted: isPromoted,
    new: !isSoldOut,
    'sold-out': isSoldOut
  }">Object Conditional Movie</h2>

  <h2 :style="{
    color: highlightColor,
    fontSize: headerSize + 'px',
    padding: '20px'
  }">Inline Style</h2>

  <h2 :style="headerStyleObject">Style Object</h2>

  <div :style="[baseStyleObject, successStyleObject]">Success Style</div>
  <div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      headingId: 'heading',
      isDisabled: false,
      status: 'success',
      isPromoted: false,
      isSoldOut: true,
      highlightColor: 'orange',
      headerSize: 50,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '10px'
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1px solid green',
        padding: '20px'
      },
      dangerStyleObject: { 
        color: 'darkred',
        backgroundColor: 'red',
        border: '1px solid darkred',
        marginTop: '5px',
      },

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

.underline {
  margin-top: 5px;
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: olivedrab;
}

.sold-out {
  color: red;
}
</style>
