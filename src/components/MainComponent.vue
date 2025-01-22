<script setup>
import Column from "/src/components/Column/Column.vue";
import CreateColumnForm from "/src/components/Column/CreateColumnForm.vue";
import { ref } from "vue";
const localStorageColumns =
  JSON.parse(localStorage.getItem("arrColumnsInLocalStorage")) || [];
const arrColumns = [
  {
    title: "to do",
    tasksCount: 0,
    order: 0,
  },

  {
    title: "Done",
    tasksCount: 0,
    order: 1,
  },
];
const savedArrayColumns = localStorageColumns.length ? localStorageColumns : arrColumns;
localStorage.setItem("arrColumnsInLocalStorage",JSON.stringify(savedArrayColumns)
);
    const draggableColumns = ref(savedArrayColumns);

    let draggedIndex = null;

    const isDraggable = (index) => {
      return index !== 0 && index !== draggableColumns.value.length - 1;
    };

    const onDragStart = (event, index) => {
      if (!isDraggable(index)) return;
      draggedIndex = index;
      event.dataTransfer.effectAllowed = "move";
    };

    const onDrop = (event, index) => {
        if (!isDraggable(index) || draggedIndex === null || !isDraggable(draggedIndex)) return;
        if (draggedIndex === index) return;
        if (draggableColumns.value.index === 0 && draggableColumns.value.length - 1) {
        draggableColumns.value.prevent
      }

      const movedColumn = draggableColumns.value[draggedIndex];
      draggableColumns.value.splice(draggedIndex, 1);
      draggableColumns.value.splice(index, 0, movedColumn);

      draggedIndex = null;
    };

</script>

<template>
  <div class="main">
    <Column
      v-for="(item, index) in draggableColumns"
      :key="index"
      :title="item.title"
      :amountTasks="item.tasksCount"

      :draggable="isDraggable(index)"
            @dragstart="onDragStart($event, index)"
            @dragover.prevent
            @drop="onDrop($event, index)"
            class="draggable-column"

      @open-modal="(taskInformation) => $emit('open-modal', taskInformation)"
    />
    <div
      class="main__create-column"
      @click="$emit('open-modal', CreateColumnForm)"
    >
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
