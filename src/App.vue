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
  },
    created() {
      const locale = localStorage.getItem('locale');
      if (locale) {
          this.$i18n.locale = locale;
      } else if (navigator.language) {
          this.$i18n.locale = navigator.language
      }
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
