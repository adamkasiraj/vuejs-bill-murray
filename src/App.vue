<template>
  <div id="app">
    <FillMurray/>
  </div>
</template>

<script>
import FillMurray from './components/FillMurray'

export default {
  name: 'App',
  components: {
    FillMurray
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
