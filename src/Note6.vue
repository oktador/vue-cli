<template>
  <h1 class="title">{{ title }}</h1>
  <Modal :title="modalTitle" :content="modalContent" theme="sale" />
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "Note6",
  components: {
    Modal,
  },
  data() {
    return {
      title: "Note 6",
      modalTitle: "Modal Title as parameter",
      modalContent: "Modal Content as parameter",
    };
  },
};
</script>
