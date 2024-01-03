<script>
 export default {
    name: 'column',
    props: {
        title: {
            type: String,
            default: ''
        }
    },
 };
</script>

<template>
    <div class='column'>
        <div class='column__header'>
            <div class='column__header-title'>{{ title }}</div>
            <div class='column__header-arrow'>
                <img alt='arrow' src='/src/assets/images/main/header-arrow.svg'>
            </div>
        </div>
        <div class='column__tasks'></div>
    </div>
</template>

<style>
.column__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-shrink: 0;
    width: 100%;
    height: 44px;
    background: var(--main-color-light-blue);
    margin-bottom: 10px;
    border-radius: 10px;
}

.column__header-title {
    display: flex;
    margin-left: 10px;
    width: auto;
    height: 20px;
    justify-content: center;
    align-items: center;
    color: var(--main-color-white);
    font-family: 'Montserrat';
    font-weight: 700;
    font-size: 16px;
    text-transform: uppercase;
    flex-shrink: 0;
}

.column__header-arrow {
    width: 24px;
    height: 24px;
    margin: 10px 14px 10px;
}

.arrow__wrapper img {
    width: 12px;
    height: 6px;
    margin-right: 10px;
}

.column__tasks {
    display: flex;
    padding: 0 18px;
    background-color: var(--main-color-white);
    min-height: 44px;
    margin-bottom: 7px;
    border-radius: 10px;
}
</style>