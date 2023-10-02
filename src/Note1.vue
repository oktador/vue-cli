<template>
  <h1 class="title">{{ title }}</h1>
</template>

<script>
export default {
  name: "Note1",
  data() {
    return {
      title: "Note 1",
    };
  },
};
</script>
<style scoped>
h1 {
  color: red;
}
</style>
