<template>
  <div id="app" class="container p-5">
    <demo-ref></demo-ref>
    <!-- <button type="button" class="btn btn-primary">Primary</button> -->
  </div>
</template>

<script>
import demoRef from './components/2ref-parent-children/demo'

export default {
  name: 'app',
  components: {
    demoRef
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
