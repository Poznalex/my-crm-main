<script>
 export default {
    name: 'column',
    props: {
        title: {
            type: String,
            default: ''
        }
    },

    data () {
        return {
            open: false
        };
    },
}
  
</script>

<template>
    <div class='column' :class="{ 'column--open': open }">
        <div class='column__header'  @click="open = !open">
            <div class='column__header-title'>{{ title }}</div>
            <img alt='arrow' src='/src/assets/images/main/column-arrow.svg'>
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

  img {
    margin-right: 14px;
}
 .column--open .column__header img {
    rotate: 180deg;
}

.column__tasks {
    display: none;
    padding: 0 18px;
    background-color: var(--main-color-white);
    min-height: 44px;
    margin-bottom: 7px;
    border-radius: 10px;
}

.column--open .column__tasks {
    display: flex;
}


@media screen and (min-width: 768px) {
    .column__header {
        width: 526px;
        height: 118px;
        float: left;
        margin: 0 10px;
        margin-bottom: 0;
        overflow: auto;
    }

    .column--open .column__tasks {
        display: none;
    }

    .column--open .column__header img {
        rotate: 0deg;
    }
}

</style>