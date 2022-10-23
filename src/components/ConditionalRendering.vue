<template>
  <!-- 条件渲染 -->
  <div>
    <button @click="awesome = !awesome">Toggle</button>
    <h1 v-if="awesome">Vue is awesome!</h1>
    <h1 v-else>Oh no 😢</h1>
  </div>
  <div>
    <div v-if="type === 'A'">A</div>
    <div v-else-if="type === 'B'">B</div>
    <div v-else-if="type === 'C'">C</div>
    <div v-else>Not A/B/c</div>
  </div>
  <div>
    <template v-if="!ok || !asd">
      <h1>Title</h1>
      <p>Paragraph 1</p>
      <p>Paragraph 2</p>
    </template>
  </div>
  <div>
    <h1 v-show="ok">Hello!</h1>
  </div>
</template>


<script>
export default {
  data() {
    return {
      awesome: false,
      type: false,
      ok: false,
      asd:false
    };
  },
};
</script>

<style>
</style>