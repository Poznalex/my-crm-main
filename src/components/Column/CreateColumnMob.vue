<script setup>
</script>

<template>
    <div class="create-column">
        <div class="create-column__text">Create Column</div>
        <form class="create-column__form">
            <label for="name">Name</label> <br>
            <input type="text" id="name" name="name">
        </form>
        <div>ADD</div>
    </div>
</template>

<style scoped>
.create-column {
    display: flex;
    flex-direction: column;
    width: 300px;
    height: 212px;
}

.create-column__text {
    margin-bottom: 18px;
    color: var(--main-color-black);
}

.create-column__form {
    margin-bottom: 32px;
    width: 100%;

}

#name {
    width: 97%;
}
</style>