<template>
  <h1 class="title">{{ title }}</h1>
  <Modal />
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "Note4",
  components: {
    Modal,
  },
  data() {
    return {
      title: "Note 4",
    };
  },
};
</script>
