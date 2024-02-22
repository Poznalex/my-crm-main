<script setup>
import { ref } from 'vue';
import Header from '/src/components/Header.vue';
import Main from '/src/components/Main.vue';
import Modal from '/src/components/Modal/Modal.vue';

const isShowModal = ref(false);
const modalComponent = ref(null);

function OpenModal(data) {
    isShowModal.value = true;
    modalComponent.value = data;
}

function CloseModal() {
    isShowModal.value = false;
    modalComponent.value = null;
}
</script>

<template>
    <Header @open-modal="OpenModal" />
    <Main @open-modal="OpenModal" />
    <Teleport to="body">
        <modal
            v-show="isShowModal"
            :defaultComponent="modalComponent"
            @close="CloseModal"
        >
        </modal>
    </Teleport>
</template>

<style scoped></style>
