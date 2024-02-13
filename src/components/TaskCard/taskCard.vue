<script setup>
    const props = defineProps(["nameProject"]);
</script>

<template>
    <div class="card">
        <img
            class="card__avatar"
            alt="user"
            src="/src/assets/images/card/avatar-card.svg"
        />
        <div class="card__texts">
            <div class="card__header">AMP Project {{ nameProject }}</div>
            <div class="card__until">Until 17.05.2021</div>
            <div class="card__hours">10 hours</div>
            <div class="card__inner-wraper"> <!-- For show inner content in row -->
                <div class="card__number">BM-675</div>
                <div class="card__project">
                    <span class="card__project-title">Project</span>X
                </div>
            </div>
        </div>
            <img class="card__arrow"
                alt="arrow"
                src="/src/assets/images/card/arrow-down.svg"
            />
    </div>
</template>

<style>
@import './TaskCard.css'
</style>