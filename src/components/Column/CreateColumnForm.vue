<script setup>
import ModalClose from '/src/components/Modal/ModalClose.vue';
</script>

<template>
    <ModalClose class="create-column__button-cancel" @close="$emit('close')" />
</template>

<style scoped>
.create-column__button-cancel {
    display: flex;
    justify-content: center;
}
</style>
