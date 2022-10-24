<template>
  <!-- 列表渲染 -->
  <div>
    <div>
      <li v-for="item in items" :key="item">
        {{ item.message }}
      </li>
    </div>
    <div>
      <li v-for="(itemas, index) in items" :key="itemas">
        {{ parentMessage }} - {{ index }} - {{ itemas.message }}
      </li>
    </div>
    <div>
      <ul>
        <li v-for="value in myObject" :key="value">
          {{ value }}
        </li>

        <li v-for="(value, key) in myObject" :key="value">
          {{ key }}<br />
          {{ value }}
        </li>
        <li v-for="(value, key, index) in myObject" :key="value">
          {{ index }}<br />
          {{ key }}<br />
          {{ value }}
        </li>
      </ul>
    </div>
    <div>
      <span v-for="n in 10" :key="n">{{ n }}</span>
    </div>
    <ul>
      <template v-for="item in items" :key="item">
        <li>{{ item.msg }}</li>
        <li class="divider" role="presentation"></li>
      </template>
    </ul>
  </div>
  <div>
    <ul>
      <template v-for="item in items" :key="item">
        <li>{{ item.msg }}</li>
        <li class="divider" role="presentation"></li>
      </template>
    </ul>
  </div>
  <div v-for="value in itaaaem" :key="value">
    {{value}}
    <!-- 内容 -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [{ message: "Foo" }, { message: "Bar" }],
      parentMessage: "Parent",
      itemas: [{ message: "Foo" }, { message: "Bar" }],
      itaaaem:[{name:'doe',id:1}],
      msg: "e2fgwqregqergqqrehgqht",
      myObject: {
        title: "How to do lists in Vue",
        author: "Jane Doe",
        publishedAt: "2016-04-10",
      },
    };
  },
};
</script>
 
<style>
li {
  list-style: none;
}
</style>