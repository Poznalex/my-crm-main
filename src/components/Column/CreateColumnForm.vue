<script setup>
import ModalClose from "/src/components/Modal/ModalClose.vue";
</script>

<template>
  <div class="create-column">
    <div class="create-column__text">Create column</div>
    <form class="create-column__form">
      <label class="create-column__form-label" for="name">Name</label>
      <br />
      <input type="text" id="name" name="name" placeholder="NEW" maxlength="75" />
    </form>
    <div class="create-column__button-add">
      <p class="create-column__button-text">Add</p>
    </div>
    <ModalClose class="create-column__button-cancel" @close="$emit('close')" />
  </div>
</template>

<style scoped>
.create-column {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.create-column__text {
  width: 100%;
  margin-bottom: 18px;
  color: var(--main-color-black);
  font-size: 20px;
  font-weight: 700;
}

.create-column__form {
  margin-bottom: 32px;
  width: 100%;
}

.create-column__form-label {
  font-size: 10px;
  color: var(--main-color-grey);
  font-weight: 600;
}

#name {
  box-sizing: border-box;
  width: 100%;
  margin-top: 4px;
  border: 1px solid var(--main-color-light-blue);
  border-radius: 4px;
  padding: 7px 12px;
}

::placeholder {
  font-size: 12px;
  font-weight: 500;
  color: var(--main-color-black);
}

.create-column__button-add {
  width: 100%;
  background-color: var(--main-color-pink);
  border-radius: 6px;
  margin-bottom: 18px;
}

.create-column__button-text {
  text-align: center;
  padding: 10px;
  font-size: 14px;
  color: var(--main-color-white);
}

.create-column__button-cancel {
  width: 50px;
}

@media screen and (min-width: 768px) {
  .create-column {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    flex-wrap: wrap;
    padding: 16px;
  }

  .create-column__text {
    width: 100%;
    margin-bottom: 32px;
    font-size: 32px;
  }

  ::placeholder {
    font-size: 14px;
  }

  #name {
    width: 100%;
  }

  .create-column__button-add {
    width: 200px;
    border-radius: 10px;
    margin-right: 42px;
    margin-bottom: 0px;
  }

  .create-column__form {
    margin-bottom: 64px;
  }

  .create-column__button-cancel {
    width: 70px;
    font-size: 20px;
    margin-right: 0px;
  }
}
</style>
>>>>>>> 3770b1a (allfix)
