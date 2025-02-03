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

const savedArrayColumns = JSON.parse(localStorage.getItem('arrColumnsInLocalStorage'));
console.log(JSON.parse(localStorage.getItem('arrColumnsInLocalStorage')));

function AddColumnToColumnArray(name) {
    const newColumn =
    {
        title: name,
        tasksCount: "0",
        order: savedArrayColumns.length - 1,
    }
    console.log(newColumn);

    savedArrayColumns.splice(savedArrayColumns.length - 1, 0, newColumn); //вставляем новую колонку  в массив колонок
    window.location.reload()
    localStorage.setItem('arrColumnsInLocalStorage', JSON.stringify(savedArrayColumns)); //сохраняем обновленный массив колонок в локал сторэдж
}
// localStorage.clear();

</script>

<template>
    <Header @open-modal="openModal" />
    <Main @open-modal="openModal" />
    <Teleport to="body">
        <Modal v-show="isShowModal" :defaultComponent="modalComponent" @close="closeModal"
            @add-new-column="AddColumnToColumnArray">
        </Modal>
    </Teleport>
</template>
<style scoped></style>
