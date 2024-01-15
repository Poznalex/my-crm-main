<script>
 export default {
    name: 'column',
    props: {
        title: {
            type: String,
            default: ''
        },

        amountTasks: {
            type: Number,
            default: ''
        },
    },

    data () {
        return {
            isOpened: false
        };
    },

    methods: {
        showTasks() {
            const isMobile = window.innerWidth < 768;
            if (isMobile) this.isOpened = !this.isOpened;
        }
  }
    
}
  
</script>

<template>
    <div class="column" :class="{ 'column--open': isOpened }">
        <div class="column__header"  @click="showTasks">
            <div class="column__header-title">{{ title }} {{ amountTasks }}</div>
            <img class="column__arrow" alt="arrow" src="/src/assets/images/main/column-arrow.svg">
        </div>
        <div class="column__tasks"></div>
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
    font-weight: 700;
    font-size: 16px;
    text-transform: uppercase;
    flex-shrink: 0;
}

 .column__arrow {
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
        align-items: start;
        width: 526px;
        height: 118px;
        margin: 0 10px;
        margin-bottom: 0;
        overflow: auto;
    }

    .column__header-title {
        font-size: 20px;
        margin: 10px 24px;
    }

    .column__tasks {
        display: flex;
        width: 526px;
        padding: 0;
        background-color: var(--main-color-white);
        min-height: 252px;
        margin: -50px 10px 0;
        border-radius: 10px;
    }

    .column__tasks {
        display: flex;
    }

    .column__arrow {
        display: none;
    }
}

</style>