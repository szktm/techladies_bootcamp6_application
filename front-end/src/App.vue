<template>
  <div id="app">
    <Mug :size="100" mood="excited" color="#A6E191" align="center"/>
    <Navigation></Navigation>
    <router-view/>
  </div>
</template>

<script>
import {Mug} from 'vue-kawaii'
import Navigation from './components/Navigation'
export default {
  name: 'App',
  components: {
    'Navigation': Navigation,
    'Mug': Mug
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
  margin-top: 60px;
}
</style>
