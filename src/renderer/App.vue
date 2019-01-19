<template>
  <div id="app">
    <nav-bar></nav-bar>
    <router-view></router-view>
  </div>
</template>

<script>
  import NavBar from './components/NavBar'

  export default {
    name: 'vue-rpg-admin',
    components: {NavBar}
  }
</script>

<style lang="sass">

</style>
