<template>
  <div>
    <p>Has published books:</p>
    <span>{{ author.books.length > 1 ? "Yes" : "No" }}</span>
  </div>
  <div>
    <p>Has published books:</p>
    <span>{{ publishedBooksMessage }}</span>
    <!-- 计算属性 -->
  </div>
  <div>
    <p>{{ calculateBooksMessage() }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      author: {
        name: "John Doe",
        books: [
          "Vue 2 - Advanced Guide",
          "Vue 3 - Basic Guide",
          "Vue 4 - The Mystery",
        ],
        firstName: "John",
        lastName: "Doe",
      },
    };
  },
  computed: {
    fullName: {
      // getter
      get() {
        return this.firstName + " " + this.lastName;
      },
      // setter
      set(newValue) {
        // 注意：我们这里使用的是解构赋值语法
        [this.firstName, this.lastName] = newValue.split(" ");
      },
    //   可写计算属性

    },
    // 一个计算属性的 getter
    publishedBooksMessage() {
      // `this` 指向当前组件实例
      return this.author.books.length > 0 ? "Yes" : "No"; // 计算属性
    },

  },
  
  methods: {
    calculateBooksMessage() {
      return this.author.books.length > 0 ? "Yes" : "No"; // 计算属性缓存 vs 方法
    },
  },
};
</script>

<style>
</style>