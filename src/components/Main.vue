<script setup>
 import Column from '/src/components/Column.vue';
</script>

<template>
    <div class='main'>
        <column title="to do -" amountTasks="18" />
        <column title="in progress -" amountTasks="3" />
        <column title="done -" amountTasks="456" />
        
        <div class='main__create-column'>
            <div class='create-column__text'>Create column</div>
            <div class='create-column__sign'>
                <img  class="create__column__plus" alt='plus' src='/src/assets/images/main/create-plus.svg'>
            </div>
        </div>
    </div> 
</template>

<style>
.main {
    display: flex;
    flex-direction: column;
    justify-content: start;
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


@media screen and (min-width: 768px) {
.main {
    display: flex;
    flex-direction: row;
    justify-content: start;
    padding: 0 24px;
    margin-top: 93px;
    overflow-x: scroll;
    }

.main__create-column {
    display: none;
    } 
}


 @media screen and (min-width: 1024px) {
   .main {
    padding: 0 60px;
    } 
 }

 @media screen and (min-width: 1400px) {
   .main {
    padding: 0 150px;
    }  
 }
    </style>