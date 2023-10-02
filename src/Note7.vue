<template>
  <h1 class="title">{{ title }}</h1>
  <br />
  <button @click="onButtonClick">Click For Open The Modal</button>
  <div v-if="showModal">
    <Modal
      :title="modalTitle"
      :content="modalContent"
      theme="sale"
      @modalClose="onModalClose"
    />
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "Note7",
  components: {
    Modal,
  },
  data() {
    return {
      title: "Note 7",
      modalTitle: "Modal Title as parameter",
      modalContent: "Modal Content as parameter",
      showModal: false,
    };
  },
  methods: {
    onButtonClick() {
      this.showModal = true;
    },
    onModalClose() {
      this.showModal = false;
    },
  },
};
</script>
