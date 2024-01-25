<script setup>

            let showModal=(ref)false;
        };
    },
    methods: {
        openModal() {
            this.showModal = true;
        },
        closeModal() {
            this.showModal = false;
        },
    },
};
</script>


<template>
    <div class="modal" v-if="showModal">
        <div class="modal-content">
            <span class="close" @click="closeModal">&times;</span>
            <p>Это модальное окно!</p>
        </div>
    </div>
</template>



<style scoped>
/* Стили для модального окна */
.modal {
    display: none;
    position: fixed;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
    background-color: #fefefe;
    margin: 15% auto;
    padding: 20px;
    border: 1px solid #888;
    width: 80%;
}

.close {
    color: #aaa;
    float: right;
    font-size: 28px;
    font-weight: bold;
    cursor: pointer;
}
</style>