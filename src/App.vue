<template>
  <div id="app">
    <app-header></app-header>
    <phone-book></phone-book>
  </div>
</template>

<script>
  import AppHeader from './components/Header'
  import PhoneBook from './components/PnoneBook'

  export default {
    components: {
      PhoneBook,
      AppHeader },
    name: 'app'
  }
</script>

<style lang="scss" scoped>
  @import "~sanitize.css";

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
