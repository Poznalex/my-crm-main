<script setup></script>

<template>
    <div class="create-column">
        <div class="create-column__title">Create column</div>
        <form class="create-column__form">
            <label class="create-column__form-label" for="name">Name</label>
            <input type="text" id="name" name="name" placeholder="NEW" maxlength="75" />
        </form>
        <button class="create-column__button-add">Add</button>
        <button class="create-column__button-cancel" @click="$emit('close')">
            Cancel
        </button>
    </div>
</template>

<style scoped>
.create-column {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.create-column__title {
    width: 100%;
    margin-bottom: 18px;
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
    margin-top: 4px;
    border: 1px solid var(--main-color-light-blue);
}

::placeholder {
    font-weight: 500;
    color: var(--main-color-black);
}

.create-column__button-add {
    width: 100%;
    background-color: var(--main-color-pink);
    font-size: 14px;
    color: var(--main-color-white);
    text-align: center;
    border-radius: 6px;
    margin-bottom: 18px;
    padding: 6px;
}

.create-column__button-cancel {
    color: var(--main-color-light-blue);
    font-size: 14px;
}

@media screen and (min-width: 768px) {
    .create-column {
        justify-content: flex-end;
        align-items: center;
        flex-wrap: wrap;
        padding: 16px;
    }

    .create-column__title {
        margin-bottom: 32px;
        font-size: 32px;
    }

    ::placeholder {
        font-size: 14px;
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
        font-size: 20px;
        margin-right: 0px;
    }
}
</style>
