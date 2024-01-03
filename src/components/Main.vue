<script setup>
 import Column from '/src/components/Column.vue';
</script>

<template>
    <div class='main'>
        <column title="to do -18" />
        <column title="in progress - 3" />
        <column title="done - 456" />
        
        <div class='main__create-column'>
            <div class='create-column__text'>Create column</div>
            <div class='create-column__sign'>
                <img alt='plus' src='/src/assets/images/main/create-plus.svg'>
            </div>
        </div>
    </div> 
</template>

<style>
.main {
    display: block;
    justify-content: center;
    padding: 0 10px;
    margin-top: 24px;
}

.main__create-column {
    display: flex;
    justify-content: center;
    align-items: center;
}

.create-column__text {
    display: flex;
    justify-content: center;
    align-items: center;
    width: auto;
    height: 18px;
    color: var(--main-color-light-blue);
}

.create-column__sign {
    display: flex;
    justify-content: center;
    width: 14px;
    height: 14px;
    margin-left: 4px;
    flex-shrink: 0;
}
</style>