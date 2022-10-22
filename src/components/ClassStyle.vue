<template>
  <div
    class="static"
    v-bind:class="{ active: isActive, 'text-danger': hasError }"
  >
    awdawd
  </div>
  <div v-bind:class="classObject">dwadawd</div>
  <div v-bind:class="classObaject"></div>
  <div v-bind:style="styleObject">aaaaaaaaaaa</div>
</template>

<script>
export default {
  data() {
    return {
      isActive: true,
      hasError: false,
      classObject: {
        active: true,
        "text-danger": false,
      },
      styleObject: {
        color: "red",
        fontSize: "13px",
      },
      error: null,
    };
  },
  computed: {
    classObaject() {
      return {
        active: this.isActive && !this.error,
        "text-danger": this.error && this.error.type === "fatal",
      };
    },
  },
};
</script>

<style>
</style>