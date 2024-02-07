<script setup>
</script>


<template>
    <div class="create-column">
        <div class="create-column__text">Create column</div>
        <form class="create-column__form">
            <label class="create-column__form-label" for="name">Name</label>
            <br />
            <input
                type="text"
                id="name"
                name="name"
                placeholder="NEW"
                maxlength="75"
                size="32"
            />
        </form>
        <div class="create-column__button">
            <p class="create-column__button-text">Add</p>
        </div>
    </div>
</template>


<style scoped>
.create-column {
    display: flex;
    flex-direction: column;
}

.create-column__text {
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

.create-column__button {
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
</style>