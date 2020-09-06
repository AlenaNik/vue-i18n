<template>
  <div id="app">
   <HelloI18n />
  </div>
</template>

<script>
import HelloI18n from './components/Helloi18n'

export default {
  name: 'App',
  components: {
    HelloI18n
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
