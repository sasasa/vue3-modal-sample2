<template>
  <button @click="openModal">Click</button>

  <Modal v-show="showModal" @modal:close="closeModal">
    これがモーダルウィンドウです。slotの中です。
  </Modal>
</template>

<script setup>
import Modal from "./components/Modal.vue";
import { ref } from "vue";
const showModal = ref(false);

const openModal = () => {
  showModal.value = true;
};

const closeModal = () => {
  showModal.value = false;
};
</script>

