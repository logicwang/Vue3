<template>
  <!-- 列表渲染 -->
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <hr>
  <TextInterpolation />
  <hr>
  <CoMputed />
  <hr>
  <ClassStyle/>
  <hr>
  <ConditionalRendering/>
  <hr>
  <ListRendering />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TextInterpolation from './components/TextInterpolation.vue'
import CoMputed from './components/CoMputed.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ClassStyle from './components/ClassStyle.vue'
import ListRendering from './components/ListRendering.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    CoMputed,
    ClassStyle,
    ConditionalRendering,
    TextInterpolation,
    ListRendering
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
