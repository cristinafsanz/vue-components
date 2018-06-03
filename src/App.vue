<template>
  <div id="app">
    <NicePictures/>
  </div>
</template>

<script>
import NicePictures from './views/NicePictures'

export default {
  name: 'App',
  components: {
    NicePictures
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 16px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
