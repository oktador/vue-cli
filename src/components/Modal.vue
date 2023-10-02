<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <slot>default value</slot>
    </div>
  </div>
</template>

<script>
export default {
  props: ["theme"],
  methods: {
    closeModal() {
      this.$emit("modalClose");
    },
  },
};
</script>

<style>
.backdrop {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background-color: white;
  border-radius: 10px;
}

.modal h1 {
  color: #03cfb4;
  border: none;
  padding: 0;
}

.modal p {
  font-style: normal;
}

.modal.sale {
  background-color: crimson;
  color: white;
}

.modal.sale h1 {
  color: white;
}
</style>
