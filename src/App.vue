<template>
  <div id="app" class="container p-5">
    <div class="alert alert-primary" v-show="show">
      消息提示
    </div>
    <!-- $refs案例 -->
    <!-- <demo-ref></demo-ref> -->

    <!-- provide案例 -->
    <demo-provide></demo-provide>
    
  </div>
</template>

<script>
// import demoRef from './components/2ref-parent-children/demo'
import demoProvide from '@/components/3provide/demo'

export default {
  provide() {
    return {
      show: this.show,
      showHide: this.showHide
    }
  },
  name: 'app',
  components: {
    // demoRef
    demoProvide
  },
  data() {
    return {
      show: false
    }
  },
  methods: {
    showHide(data) {
      this.show = data;
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
