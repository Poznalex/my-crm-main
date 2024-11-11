<script setup>
import Column from '/src/components/Column/Column.vue';
import CreateColumnForm from '/src/components/Column/CreateColumnForm.vue';
const arrColumns = [
    {
         title: "to do",
         tasksCount: "18",
         order: "0",
    },

    {
         title: "in progress",
         tasksCount: "3",
         order: "1",
    },

    {
         title: "Done",
         tasksCount: "456",
         order: "2",
    },

]

localStorage.setItem('arrColumns', JSON.stringify(arrColumns));
</script>

<template>
    <div class="main">

        <Column 
        v-for="(item, index) in arrColumns"
        :key="index"
        :title="item.title"
        :amountTasks="item.tasksCount"
         @open-modal="(taskInformation) => $emit('open-modal', taskInformation)"
/>
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
