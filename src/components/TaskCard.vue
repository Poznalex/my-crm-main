<script>
export default {
    name: 'taskcard'
}
</script>

<template>
    <div class="card__wrapper">
        <div class="card__content">
            <img class="card__avatar" alt="user" src="/src/assets/images/card/AVATAR 1.svg">
            <div class="card__info__wrapper">
                <div class="card__header">AMP Project X</div>
                <div class="card__until">Until 17.05.2021</div>
                <div class="card__hours">10 hours</div>
                <div class="card__inner__wrapper">
                    <div class="card__number">BM-675</div>
                    <div class="card__project">
                        <span class="card__project__title">Project</span>X
                    </div>
                </div>
            </div>
        </div>
        <div class="card__arrow">
            <img class="arrow__down" alt="arrow" src="/src/assets/images/card/Arrow down.svg">
        </div>
    </div>
</template>

<style>
.card__wrapper {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: space-between;
} 

.card__content {
    display: flex;
    align-items: center;
}
    
.card__avatar {
    margin: 6px 0;
    margin-left: 10px;
    margin-right: 12px;
}

.card__info__wrapper {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    align-content: flex-start;
    width: 100%;
}

.card__header {
    display: flex;
    align-items: center;
    width: 100%;
    height: 14px;
    color: var(--main-color-black);
    font-size: 14px;
    font-weight: 600;
}

.card__until {
    display: none;
}

.card__hours {
    display: none;
}

.card__inner__wrapper {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-top: 6px;
}

.card__number {
    display: flex;
    width: 40px;
    height: 10px;
    flex-direction: column;
    justify-content: center;
    margin-right: 8px;
    font-size: 10px;
    font-weight: 600;
    color: var(--main-color-grey);
}

.card__project {
    display: flex;
    width: 12px;
    height: 12px;
    background: var(--main-color-transp-blue);
    color: var(--main-color-blue);
    font-size: 8px;
    border-radius: 4px;
    justify-content: center;
    align-items: center;
} 

.card__project__title {
    display: none;
    margin-right: 6px;
}

.card__arrow {
    display: flex;
    width: 64px;
    height: 24px;
    justify-content: flex-end;
}


@media screen and (min-width: 768px) {
.card__wrapper {
    display: flex;
    flex-direction: column;
    position: relative;
    justify-content: flex-start;
    align-items: flex-start;
    margin: 24px;
}

.card__header {
    font-size: 20px;
    font-weight: 600;
    line-height: 30px;
    margin-bottom: 16px;
}

.card__until {
    display: flex;
    width: 121px;
    height: 20px;
    font-size: 16px;
    font-weight: 500;
    color: var(--main-color-grey);
}

.card__hours {
    display: flex;
    width: 68px;
    height: 20px;
    font-size: 16px;
    font-weight: 500;
    color: var(--main-color-grey);
    margin-bottom: 16px;
}

.card__avatar {
    position: absolute;
    bottom: 24px;
    right: 24px;
    margin: 0;
}

.card__arrow {
    display: none;
}

.card__inner__wrapper {
    width: 478px;
    height: 96px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.card__number {
    width: 96px;
    height: 30px;
    font-size: 24px;
    font-weight: 600;
    color: var(--main-color-black);
    order: 2;
}

.card__project {
    width: 110px;
    height: 34px;
    padding: 8px 18px;
    font-size: 16px;
    font-weight: 500;
    line-height: 18px;
    border-radius: 10px;
    order: 1;
    margin-bottom: 32px;
}

.card__project__title {
    display: flex;
}

}
</style>