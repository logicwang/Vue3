<template>
  <div>
    <button @click="count++">点击增加: {{ count }}</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
};
</script>

<style>
</style>