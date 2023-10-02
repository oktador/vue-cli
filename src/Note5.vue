<template>
  <h1 class="title">{{ title }}</h1>
  <!--Modal title="Modal Title as parameter" content="Modal Content as parameter" /-->
  <Modal :title="modalTitle" :content="modalContent" />
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "Note5",
  components: {
    Modal,
  },
  data() {
    return {
      title: "Note 5",
      modalTitle: "Modal Title as parameter",
      modalContent: "Modal Content as parameter",
    };
  },
};
</script>
