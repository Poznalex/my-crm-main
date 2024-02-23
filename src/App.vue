<script setup>
import { ref } from 'vue';
import Header from '/src/components/Header.vue';
import Main from '/src/components/Main.vue';
import Modal from '/src/components/Modal/Modal.vue';

const isShowModal = ref(false);
const modalComponent = ref(null);

function openModal(data) {
    isShowModal.value = true;
    modalComponent.value = data;
}

function closeModal() {
    isShowModal.value = false;
    modalComponent.value = null;
}
</script>

<template>
    <Header @open-modal="openModal" />
    <Main @open-modal="openModal" />
    <Teleport to="body">
        <Modal
            v-show="isShowModal"
            :defaultComponent="modalComponent"
            @close="closeModal"
        >
        </Modal>
    </Teleport>
</template>

<style scoped></style>
