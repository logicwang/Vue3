<template>
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <hr>
  <TextInterpolation />
  <hr>
  <CoMputed />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TextInterpolation from './components/TextInterpolation.vue'
import CoMputed from './components/CoMputed.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    CoMputed,
    TextInterpolation
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
