<script setup></script>

<template>
    <div class="modal__button" @click="$emit('close')">Cancel</div>
</template>

<style scoped>
.modal__button {
    color: var(--main-color-light-blue);
    font-size: 14px;
}
</style>
