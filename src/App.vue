<template>
  <NavBar/>
  <MainPage/>
</template>

<script>
import MainPage from './components/MainPage.vue'
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',
  components: {
    MainPage,
    NavBar
  }
}
</script>

<style>
#app {
  margin: 0;
  padding: 0;
}
</style>
