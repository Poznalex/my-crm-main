<script setup>
import { ref } from 'vue';
import Header from '/src/components/Header.vue';
import Main from '/src/components/MainComponent.vue';
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

const savedArrayColumns = JSON.parse(localStorage.getItem('arrColumns')) || [];

function AddColumnToColumnArray(name) {
    const newColumn =
    {
         title: name,
         tasksCount: "0",
         order: savedArrayColumns.length-1,
    };
    savedArrayColumns.splice(savedArrayColumns.length-1, 0, newColumn); //вставляем новую колонку  в массив колонок
    localStorage.setItem('arrColumns', JSON.stringify(savedArrayColumns)); //сохраняем обновленный массив колонок в локал сторэдж
}

function addColumnNew(e) {
  alert(e);
}// press buttton create column/add
</script>

<template>
    <Header @open-modal="openModal" />
    <Main
        :localStorageColumns="savedArrayColumns"  
        @open-modal="openModal" 
    />
    <Teleport to="body">
        <Modal
            v-show="isShowModal"
            :defaultComponent="modalComponent"
            @close="closeModal"
            @add-new-column="addColumnNew"
        >
        </Modal>
    </Teleport>
</template>
<style scoped></style>
