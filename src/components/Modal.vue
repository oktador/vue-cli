<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <slot>default value</slot>
      <div class="actions">
        <slot name="links"></slot>
      </div>
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

.modal .actions {
  text-align: center;
  margin: 30px 0 10px 0;
}

.modal .actions a {
  color: #333;
  margin: 10px;
  padding: 8px;
  border: 1px solid #afafaf;
  border-radius: 4px;
  text-decoration: none;
  background-color: #dadada;
}

.modal.sale {
  background-color: crimson;
  color: white;
}

.modal.sale h1 {
  color: white;
}

.modal.sale .actions {
  color: white;
}

.modal.sale .actions a {
  color: white;
  background-color: crimson;
}
</style>
