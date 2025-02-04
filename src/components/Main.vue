<script setup>
import Column from '/src/components/Column/Column.vue';
import CreateColumnForm from '/src/components/Column/CreateColumnForm.vue';
</script>

<template>
    <div class="main">
        <div class="columns-wrapper">
            <Column
                title="to do"
                amountTasks="18"
                @open-modal="(taskInformation) => $emit('open-modal', taskInformation)"
            />
            <Column
                title="in progress"
                amountTasks="3"
                @open-modal="(taskInformation) => $emit('open-modal', taskInformation)"
            />
            <Column
                title="done"
                amountTasks="456"
                @open-modal="(taskInformation) => $emit('open-modal', taskInformation)"
            />
        </div>
        <div class="main__create-column" @click="$emit('open-modal', CreateColumnForm)">
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
    justify-content: center;
    align-items: center;
}

.main__create-column {
    display: flex;
    align-items: center;
    cursor: pointer;
}

.columns-wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
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
        justify-content: unset;
        align-items: unset;
        padding: 93px 24px 0;
        flex-grow: 1;
        overflow: hidden;
    }

    .main__create-column {
        display: none;
    }

    .columns-wrapper {
        display: flex;
        flex-direction: row;
        overflow: scroll;
    }

    .columns-wrapper::-webkit-scrollbar {
        width: 6px;
        height: 6px;
    }

    .columns-wrapper::-webkit-scrollbar-thumb {
        border-radius: 8px;
        background: var(--main-color-light-blue);
    }

    .columns-wrapper::-webkit-scrollbar-track {
        border-radius: 8px;
        background-color: var(--main-color-white);
    }

    .columns-wrapper::-webkit-scrollbar-corner,
    .columns-wrapper::-webkit-scrollbar-track:horizontal {
        background-color: transparent;
        margin-right: 20px;
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
