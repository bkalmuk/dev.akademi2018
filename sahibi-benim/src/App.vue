<template>
  <div id="app">
    <carousel></carousel>
    <navnav></navnav>
    <users></users>
    <categories></categories>
  </div> 
</template>

<script>
import Carousel from './components/Carousel.vue'
import Navnav from './components/Navnav.vue'
import Users from './components/Users.vue'

export default {
  name: 'app',
  components: { Carousel, Navnav, Users },
  data () {
    return {
   
    }
  },
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
