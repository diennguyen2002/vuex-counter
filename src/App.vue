<template>
  <div id="app">
    <div> Current count: {{ $store.state.count }} is {{ evenOrOdd }} number</div>
    <controls />
  </div>
</template>

<script>
import {mapGetters} from 'vuex'
import Controls from './components/Controls'
export default {
  name: 'app',
  components:{
    Controls
  },
  computed: mapGetters([
    'evenOrOdd'
  ])
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
