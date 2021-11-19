<template>
  <div class="backdrop" @click.self="closeModal()">
    <div class="modal">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    closeModal() {
      this.$emit('closeModal');
    },
  },
};
</script>

<style scoped>
h1 {
  color: coral;
}
.modal {
  max-width: 600px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}
.backdrop {
  top: 0;
  left: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
</style>
