<template>
  <h1 class="title">{{ title }}</h1>
  <br />
  <input type="text" ref="input1" />
  <button @click="onButtonClick">Click Me To Focus On Input</button>
</template>

<script>
export default {
  name: "Note3",
  data() {
    return {
      title: "Note 3",
    };
  },
  methods: {
    onButtonClick() {
      this.$refs.input1.focus();
    },
  },
};
</script>
