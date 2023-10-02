<template>
  <h1 class="title">{{ title }}</h1>
  <br />
  <button @click="onButton1Click">Click For Open The Modal 1</button>
  <br />
  <button @click="onButton2Click">Click For Open The Modal 2</button>
  <Modal theme="notsale" @modalClose="onModalClose" v-if="currentModal === 1">
    <h1>{{ modalTitles[0] }}</h1>
    <p>{{ modalContents[0] }}</p>
    <template v-slot:links>
      <a href="#">Link1</a>
      <a href="#">Link2</a>
    </template>
  </Modal>
  <Modal theme="sale" @modalClose="onModalClose" v-else-if="currentModal === 2">
    <h1>{{ modalTitles[1] }}</h1>
    <p>{{ modalContents[1] }}</p>
    <template v-slot:links>
      <a href="#">Link1</a>
      <a href="#">Link2</a>
    </template>
  </Modal>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "Note11",
  components: {
    Modal,
  },
  data() {
    return {
      title: "Note 11",
      modalTitles: ["Modal 1 Title", "Modal 2 Title"],
      modalContents: ["Modal 1 Content", "Modal 2 Content"],
      currentModal: 0,
    };
  },
  methods: {
    onButton1Click() {
      this.currentModal = 1;
    },
    onButton2Click() {
      this.currentModal = 2;
    },
    onModalClose() {
      this.currentModal = 0;
    },
  },
};
</script>
