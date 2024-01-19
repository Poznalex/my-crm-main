<script setup>
import Column from "/src/components/Column.vue";
</script>

<template>
    <div class="main">
        <column title="to do" amountTasks="18" />
        <column title="in progress" amountTasks="3" />
        <column title="done" amountTasks="456" />

        <div class="main__create-column">
            <div class="create-column__text">Create column</div>
            <div class="create-column__icon">
                <img alt="plus" src="/src/assets/images/main/create-plus.svg" />
            </div>
        </div>
    </div>
</template>

<style>
.main {
    display: flex;
    flex-direction: column;
    padding: 24px 10px 0;
}

.main__create-column {
    display: flex;
    justify-content: center;
    align-items: center;
}

.create-column__text {
    width: auto;
    line-height: 18px;
    color: var(--main-color-light-blue);
}

.create-column__icon {
    display: flex;
    justify-content: center;
    width: 14px;
    height: 14px;
    margin-left: 4px;
    flex-shrink: 0;
}

@media screen and (min-width: 768px) {
    .main {
        flex-direction: row;
        padding: 93px 24px 0;
        overflow-x: scroll;
    }

    .main__create-column {
        display: none;
    }
}

@media screen and (min-width: 1024px) {
    .main {
        padding: 93px 60px 0;
    }
}

@media screen and (min-width: 1400px) {
    .main {
        padding: 93px 150px 0;
    }
}
</style>
