<script>
export default {
    name: "taskcard",
    props: {
        nameProject: {
            type: String,
            default: "",
        },
    },
};
</script>

<template>
    <div class="card">
        <img
            class="card__avatar"
            alt="user"
            src="/src/assets/images/card/AVATAR 1.svg"
        />
        <div class="card__info__wrapper">
            <div class="card__header">AMP Project {{ nameProject }}</div>
            <div class="card__until">Until 17.05.2021</div>
            <div class="card__hours">10 hours</div>
            <div class="card__inner__wrapper">
                <div class="card__number">BM-675</div>
                <div class="card__project">
                    <span class="card__project__title">Project</span>X
                </div>
            </div>
        </div>
        <div class="card__arrow">
            <img
                class="arrow__down"
                alt="arrow"
                src="/src/assets/images/card/Arrow down.svg"
            />
        </div>
    </div>
</template>

<style>
@import './TaskCard.css'
</style>