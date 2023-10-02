<template>
  <h1 class="title">{{ title }}</h1>
  <br />
  <button @click="onButtonClick">Click For Open The Modal</button>
  <div v-if="showModal">
    <Modal theme="sale" @modalClose="onModalClose"></Modal>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "Note8",
  components: {
    Modal,
  },
  data() {
    return {
      title: "Note 8",
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
