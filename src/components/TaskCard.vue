<script>
export default {
    name: "taskcard",
    props: {
        nameProject: {
            type: String,
            default: "",
        },
    },
};
</script>

<template>
    <div class="card">
        <img
            class="card__avatar"
            alt="user"
            src="/src/assets/images/card/AVATAR 1.svg"
        />
        <div class="card__info__wrapper">
            <div class="card__header">AMP Project {{ nameProject }}</div>
            <div class="card__until">Until 17.05.2021</div>
            <div class="card__hours">10 hours</div>
            <div class="card__inner__wrapper">
                <div class="card__number">BM-675</div>
                <div class="card__project">
                    <span class="card__project__title">Project</span>X
                </div>
            </div>
        </div>
        <div class="card__arrow">
            <img
                class="arrow__down"
                alt="arrow"
                src="/src/assets/images/card/Arrow down.svg"
            />
        </div>
    </div>
</template>

<style>
.card {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: auto;
    min-height: 44px;
    margin-bottom: 12px;
    border-radius: 10px;
    background-color: var(--main-color-white);
}

.card__avatar {
    margin: 6px 0;
    margin-left: 10px;
    margin-right: 12px;
}

.card__info__wrapper {
    display: flex;
    flex-direction: column;
    width: 100%;
    min-width: 0;
}

.card__header {
    display: block;
    width: auto;
    height: 14px;
    color: var(--main-color-black);
    font-size: 14px;
    font-weight: 600;
    flex-shrink: 0;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
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
    width: auto;
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
    justify-content: center;
    align-items: center;
    width: 12px;
    height: 12px;
    background: var(--main-color-transp-blue);
    color: var(--main-color-blue);
    font-size: 8px;
    border-radius: 4px;
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
    .card {
        position: relative;
        width: 100%;
        display: flex;
        margin-bottom: 12px;
        height: auto;
        max-height: auto;
        border-radius: 10px;
        padding: 24px;
        flex-direction: column;
    }

    .card__info__wrapper {
        min-height: 204px;
    }
    .card__header {
        display: flex;
        width: 100%;
        height: auto;
        white-space: normal;
        font-size: 20px;
        font-weight: 600;
        line-height: 30px;
        margin-bottom: 16px;
    }

    .card__until {
        display: flex;
        width: 121px;
        height: 20px;
        margin-bottom: 6px;
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
        width: 50px;
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
        margin-top: 0;
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
        margin-bottom: 35px;
    }

    .card__project__title {
        display: flex;
    }
}
</style>