<script setup>
const props = defineProps({
    defaultComponent: {
        type: Object,
        default: null,
    },
});
</script>

<template>
    <Transition name="modal">
        <div class="modal-mask">
            <div v-if="defaultComponent" class="modal-container">
                <component :is="defaultComponent" />
                <div class="modal-container__button-wraper">
                    <button class="modal-default-button" @click="$emit('close')">
                        Cancel
                    </button>
                </div>
            </div>
        </div>
    </Transition>
</template>



<style scoped>
.modal-mask {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    transition: opacity 0.3s ease;
}

.modal-container {
    width: auto;
    margin: auto;
    padding: 16px 12px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
    transition: all 0.3s ease;
}

.modal-container__button-wraper {
    display: flex;
    justify-content: center;
}

.modal-default-button {
    color: var(--main-color-light-blue);
    font-size: 14px;
}

.modal-enter-from {
    opacity: 0;
}

.modal-leave-to {
    opacity: 0;
}
</style>