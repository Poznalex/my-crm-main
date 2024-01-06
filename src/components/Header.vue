<script setup></script>

<template>
    <div class="header">
        <div class="header__logo">
            <img alt="logo" src="/src/assets/images/header/logo-header.svg">
        </div>
        <button class="header__button btn-column">Create column</button>
        <button class="header__button btn-task">Create task</button>
        <div class="header__plus">
            <img alt="logo" src="/src/assets/images/header/icon-plus.svg">
        </div>
    </div>
</template>

<style scoped>
.header {
    display: flex;
    background: var(--main-color-white);
    align-items: center;
    height: 62px;
    padding: 0 10px;
}

.header__logo { 
    margin-right: auto;
    width: 140px;
    height: 42px;
}

.header__logo img {
    width: 100%;
    height: 100%;
}

.header__button {
    display: none;
    width: 234px;
    height: 48px;
    justify-content: center;
    align-items: center;
    border-radius: 10px;
    font-family: 'Montserrat';
    font-size: 20px;
    font-weight: 500;
    padding: 12px 18px;
}

.btn-column {
    border: 1px solid var(--main-color-blue);
    margin: 0 32px;
    color: var(--main-color-blue);
}

.btn-column:hover {
    color: var(--main-color-light-blue);
    border-color: var(--main-color-light-blue);
}

.btn-column:active {
    background: var(--main-color-light-blue);
    color: var(--main-color-white);
}

.btn-task {
    background: var(--main-color-pink);
    color: var(--main-color-white);
}

.btn-task:hover {
    background: var(--main-color-transp-pink);
}

.btn-task:active {
    background: var(--main-color-dark-pink);
}

@media screen and (min-width: 768px) {
   .header {
        display: flex;
        padding: 0 24px;
        height: 122px;
    }
  
    .header__logo {
        width: 308px;
        height: 94px; 
    }

    .header__plus {
        display: none;
    }

    .header__button {
        display: flex;
    }
}

@media screen and (min-width: 1024px) {
    .header {
        padding: 0 60px;
    }
}

@media screen and (min-width: 1400px) {
    .header {
        padding: 0 150px;
    }
}
</style>