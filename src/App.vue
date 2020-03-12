<template>
  <div id="app">
    <svg-line-chart/>
  </div>
</template>

<script>
import SvgLineChart from './components/SvgLineChart.vue'

export default {
  name: 'App',
  components: {
    SvgLineChart
  }
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
