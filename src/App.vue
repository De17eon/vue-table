<template>
  <div id="app">
      <h1>Change json objects using tabular web interface</h1>
      <v-wrapper/>
  </div>
</template>

<script>
import vWrapper from './components/v-wrapper'

export default {
  name: 'App',
  components: {
    vWrapper,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
