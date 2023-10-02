<template>
  <h1 class="title">{{ title }}</h1>
  <br />
  <button @click="onButtonClick">Click For Open The Modal</button>
  <div v-if="showModal">
    <Modal theme="" @modalClose="onModalClose">
      <h1>{{ modalTitle }}</h1>
      <p>{{ modalContent }}</p>
      <template v-slot:links>
        <a href="#">Link1</a>
        <a href="#">Link2</a>
      </template>
    </Modal>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "Note10",
  components: {
    Modal,
  },
  data() {
    return {
      title: "Note 10",
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
