<template>
  <div id="app">
    <data-flow></data-flow>
  </div>
</template>

<script>
import dataFlow from './components/dataFlow'

export default {
  name: 'app',
  components: {
    dataFlow
  }
}
</script>

<style>
#app {
  display: flex;
  justify-content: center;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
