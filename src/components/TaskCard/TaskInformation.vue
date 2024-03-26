<script setup></script>

<template>
    <div class="task">
        <div class="task__header">
            <div class="task__number">BM-675</div>
            <button class="task__close" @click="$emit('close')">
                <img alt="button close" src="/src/assets/images/card/close.svg" />
            </button>
        </div>
        <div class="task__project">
            <div class="task__project-name">AMP Project X</div>
            <div class="task__user-desktop">
                <div class="task__user-name">Abdul</div>
                <img
                    class="task__user-avatar"
                    alt="avatar"
                    src="/src/assets/images/card/user-avatar.svg"
                />
            </div>
        </div>
        <div class="task__description">
            <div class="task__description-title">Description</div>
            <div class="task__description-content">
                12.05.Rosemary Fell was not exactly beautiful. She was young, brilliant,
                extremely modern, well dressed and amazingly well read in the newest of
                the new books. Rosemary had been married two years, and her husband was
                very fond of her. They were rich, really rich, not just comfortably
                well-off, so if Rosemary wanted to shop, she would go to Paris as you and
                I would go to Bond Street.
            </div>
        </div>
        <div class="task__date">
            <div class="task__until">
                <img alt="calendar" src="/src/assets/images/card/calendar.svg" />
                <div class="task__until-date">Until 17.05.2021</div>
            </div>
            <div class="task__estimate">
                <img alt="clock" src="/src/assets/images/card/clock .svg" />
                <div class="task__estimate-date">Estimation time 10h</div>
            </div>
            <div class="task__created">
                <div class="task__created-date">Created 11 March 2021, 11:55</div>
                <div class="task__user-mob">
                    <img
                        class="task__user-avatar"
                        alt="avatar"
                        src="/src/assets/images/card/user-avatar.svg"
                    />
                </div>
            </div>
        </div>
    </div>
</template>

<style>
@import './TaskInformation.css';
</style>
