<template>
  <div id="app">
    <div> Current count: {{ count }} is {{ evenOrOdd }} number</div>
    <controls />
  </div>
</template>

<script>
import {mapGetters, mapState} from 'vuex'
import Controls from './components/Controls'
export default {
  name: 'app',
  components:{
    Controls
  },
  computed: {
    ...mapGetters(['evenOrOdd']),
    ...mapState(['count']),
  }
  // computed: mapGetters([
  //   'evenOrOdd'
  // ]),
  // computed: mapState({
  //   count: 'count',
  //   evenOrOdd: function(){
  //     return this.$store.getters.evenOrOdd
  //   }
  // })
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
