<script setup></script>

<template>
    <div class="header">
      <div class="header__item header__logo">
        <img alt="logo" src="/src/assets/images/logo-header.svg">
      </div>
      <button class="header__item header__button btn-column">Create column</button>
      <button class="header__item header__button btn-task">Create task</button>
      <div class="header__item header__plus">
        <img alt="logo" src="/src/assets/images/icon-plus.svg">
      </div>
    </div>
</template>

<style scoped>
  .header {
    display: flex;
    justify-content: space-around;
    padding-right: 150px;
    padding-left: 150px;
    height: 122px;
    background: var(--main-color-white);
    align-items: center;
  }

  .header__item {
    display: flex;
   }

  .header__button {
    width: 234px;
    height: 48px;
    border: 1px solid #3F89FC;
    justify-content: center;
    align-items: center;
    border-radius: 10px;
    font-family: 'Montserrat';
    font-size: 20px;
    font-weight: 500;
    padding: 12px 18px;
  }

  .header__logo { 
    margin-right: auto;
    width: 307.95px;
    height: 94px;
    }

  .btn-column {
    margin-right: 32px;
    margin-left: 32px;
    color: var(--main-color-blue);
   }
  
  .btn-column:hover {
    color: var(--main-color-hover-blue);
    border-color: var(--main-color-hover-blue);
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

  @media screen and (max-width: 768px) {
  .header__button {
    display: none;
   }
   
   .header {
    height: 62px;
    padding-left: 10px;
    padding-right: 10px;
  }
  .header__logo {
    width: 140px;
    height: 42px;
   }
  }
  .header__plus {
  padding: 0;
  border: 0;
  }

  @media screen and (min-width: 768px) {
    .header__plus {
      display: none;
    }
  }
</style>