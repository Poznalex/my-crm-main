<script setup></script>

<template>
    <div class='wrapper'>
        <div class='column__wrapper'>
            <div class='header__column'>
                <div class='header__content'>TO DO-18</div>
                <div class='arrow__wrapper'>
                    <img alt='arrow' src='/src/assets/images/arrow.svg'>
                </div>
            </div>
            <div class='task__wrapper'>
                <p>Happy 2024 year!</p>
            </div>
        </div>
        <div class='column-wrapper'>
            <div class='header__column'>
                <div class='header__content'>IN PROGRESS-3</div>
                <div class='arrow__wrapper'>
                    <img alt='arrow' src='/src/assets/images/arrow.svg'>
                </div>
            </div>
            <div class='task__wrapper'>
                <p>Happy 2024 year!</p>
            </div>
        </div>
        <div class='column-wrapper'>
            <div class='header__column'>
                <div class='header__content'>DONE-456</div>
                <div class='arrow__wrapper'>
                    <img alt='arrow' src='/src/assets/images/arrow.svg'>
                </div>
            </div>
            <div class='task__wrapper'>
                <p>Happy 2024 year!</p>
            </div>
        </div>
        <div class='btn__create__column__wrapper'>
            <div class='btn__create__column'>Create column</div>
            <div class='sign__create__column'>
                <img alt='plus' src='/src/assets/images/plus for create column-mob.svg'>
            </div>
        </div>
    </div> 
</template>

<style>
.wrapper {
    display: block;
    justify-content: center;
    padding: 0 10px;
    margin-top: 24px;
}

.header__column {
    display: flex;
    justify-content: space-between;
    flex-shrink: 0;
    width: 100%;
    height: 44px;
    background: var(--main-color-light-blue);
    margin-bottom: 10px;
    border-radius: 10px;
}

.header__content {
    display: block;
    margin-top: 12px;
    margin-left: 10px;
    display: flex;
    width: 204px;
    height: 20px;
    justify-content: left;
    align-items: center;
    flex-shrink: 0;
    color: var(--main-color-white);
    font-family: 'Montserrat';
    font-weight: 700;
    font-size: 16px;
}

.arrow__wrapper {
    width: 24px;
    height: 24px;
    margin: 10px 14px 10px;
}

.arrow__wrapper img {
    width: 12px;
    height: 6px;
}

.task__wrapper {
    display: none;
    padding: 0 18px;
    background-color: white;
    min-height: 44px;
    margin-bottom: 7px;
}

.btn__create__column__wrapper {
    display: flex;
    margin-left: 87px;
}

.btn__create__column {
    display: flex;
    justify-content: center;
    width: 108px;
    height: 18px;
    color: var(--main-color-light-blue);
    font-family: Montserrat;
    font-size: 14px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
}

.sign__create__column {
    display: flex;
    width: 14px;
    height: 14px;
    margin-left: 4px;
    margin-top: 2px;
    margin-bottom: 2px;
    flex-shrink: 0;
}
</style>