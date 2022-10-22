<template>
  <div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 1,
      someObject: {},
    };
  },

  mounted() { // `mounted` 是生命周期钩子，之后我们会讲到
    console.log(this.count); // => 1   // `this` 指向当前组件实例
    this.count = 2; // 数据属性也可以被更改

    const newObject = {};
    this.someObject = newObject;
    console.log(newObject === this.someObject); // false
  },
};
</script>

<style>
</style>