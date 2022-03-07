<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Home from './view/Home.vue'

export default {
  name: 'app',
  components: {
    Home
  }
}
</script>

<style scoped>
#app{
  padding: 0;
  margin: 0;
}
</style>
