<script setup>
import Header from "/src/components/Header.vue"
import Main from "/src/components/Main.vue"
// import Modal from"/src/components/Modal.vue"

// export default {
//     components: {
//     Modal,
//   },
  
//   methods: {
//     openModal() {
//       this.$refs.modal.openModal();
//     },
//   },
// };
</script>

<template>
    <Header />
    <Main />
    <!-- <button @click="openModal">Открыть модальное окно</button> -->
    <!-- <modal /> -->
</template>

<style scoped>
button {
    border: 1px solid black;
}
</style>
