<script setup>
import { ref } from 'vue';
import TaskCard from '/src/components/TaskCard/TaskCard.vue';

const props = defineProps(['title', 'amountTasks']);
let isOpened = ref(false);
const showTasks = () => {
    if (window.innerWidth < 768) isOpened.value = !isOpened.value;
};
</script>

<template>
    <div class="column" :class="{ 'column--open': isOpened }">
        <div class="column__header" @click="showTasks">
            <div class="column__header-title">{{ title }} - {{ amountTasks }}</div>
            <img
                class="column__arrow"
                alt="arrow"
                src="/src/assets/images/main/column-arrow.svg"
            />
        </div>
        <div class="column__tasks">
            <TaskCard
                projectName="X"
                @open-modal="(taskInformation) => $emit('open-modal', taskInformation)"
            />
            <TaskCard
                projectName="X"
                @open-modal="(taskInformation) => $emit('open-modal', taskInformation)"
            />
            <TaskCard
                projectName="X"
                @open-modal="(taskInformation) => $emit('open-modal', taskInformation)"
            />
        </div>
    </div>
</template>

<style>
.column {
    width: 100%;
}

.column__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 44px;
    background: var(--main-color-light-blue);
    margin-bottom: 10px;
    border-radius: 10px;
    padding: 10px 14px 10px 10px;
}

.column__header-title {
    width: auto;
    justify-content: center;
    align-items: center;
    color: var(--main-color-white);
    font-weight: 700;
    font-size: 16px;
    text-transform: uppercase;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}

.column__arrow {
    margin-left: 14px;
}

.column--open .column__header img {
    rotate: 180deg;
}

.column__tasks {
    display: none;
    margin-bottom: 10px;
}

.column--open .column__tasks {
    display: block;
}

@media screen and (min-width: 768px) {
    .column {
        margin-right: 20px;
        width: 526px;
        flex-shrink: 0;
    }

    .column__header {
        align-items: start;
        height: 118px;
        padding: 10px 24px;
    }

    .column__header-title {
        font-size: 20px;
    }

    .column__tasks {
        display: block;
        margin-top: -58px;
    }

    .column__arrow {
        display: none;
    }
}
</style>
