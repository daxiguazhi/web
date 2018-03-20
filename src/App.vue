<template>
  <div id="app">
    <!--<home></home>-->
    <router-link :to="{name: 'Home'}">Home</router-link>
    <router-view/>
  </div>
</template>

<script>
import home from '@/page/home'
export default {
  name: 'App',
  data () {
    return {}
  },
  components: {
    home
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
  /*margin-top: 60px;*/
}
</style>
