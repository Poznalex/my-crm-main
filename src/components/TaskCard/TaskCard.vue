<script setup>
import TaskInformation from '/src/components/TaskCard/TaskInformation.vue';

const props = defineProps(['projectName']);
</script>

<template>
    <div class="card" @click="$emit('open-modal', TaskInformation)">
        <img
            class="card__avatar"
            alt="user"
            src="/src/assets/images/card/avatar-card.svg"
        />
        <div class="card__texts">
            <div class="card__header">AMP Project</div>
            <div class="card__until">Until 17.05.2021</div>
            <div class="card__hours">10 hours</div>
            <div class="card__inner-wraper">
                <div class="card__number">BM-675</div>
                <div class="card__project">
                    <span class="card__project-title">Project</span>{{ projectName }}
                </div>
            </div>
        </div>
        <img
            class="card__arrow"
            alt="arrow"
            src="/src/assets/images/card/arrow-down.svg"
        />
    </div>
</template>

<style>
@import './TaskCard.css';
</style>
