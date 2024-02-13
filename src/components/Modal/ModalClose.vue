<script setup>
</script>

<template>
   
        <div class="modal-default-button" @click="$emit('close')">
            Cancel
        </div>
</template>

<style scoped>

.modal-default-button {
    color: var(--main-color-light-blue);
    font-size: 14px;
}
</style>