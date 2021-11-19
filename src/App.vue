<template>
  <button @click="toggleShowModal()">Show Modal</button>
  <div v-if="showModal">
    <Modal :title="title" :content="content" @closeModal="toggleShowModal()" />
  </div>
</template>

<script>
import Modal from './components/Modal.vue';

export default {
  name: 'App',
  components: {
    Modal,
  },
  data() {
    return {
      showModal: false,
      title: 'Some title for this content!',
      content: 'This is some lorem ipsum like filler content for this property',
    };
  },
  methods: {
    toggleShowModal() {
      this.showModal = !this.showModal;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
