<template>
  <div id="app">
    <SimpleBlock/>
  </div>
</template>

<script>
import SimpleBlock from './components/SimpleBlock'

require('typeface-nunito')

export default {
  name: 'App',
  components: {
    SimpleBlock
  }
}
</script>

<style>
#app {
  font-family: 'Nunito', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100%;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
