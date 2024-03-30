<script setup></script>

<template>
    <div class="wrapper">
        <div class="title">Create task</div>
        <form class="input-forms">
            <div class="name">
                <label class="name-title" for="name">Name</label>
                <input
                    class="name-input"
                    type="text"
                    name="name"
                    placeholder="Placeholder"
                    maxlength="500"
                />
            </div>
            <div class="description">
                <label class="description-title" for="description">Description</label>
                <div class="description-header">
                    <span>b</span>
                    <span>i</span>
                    <span>u</span>
                </div>
                <textarea
                    placeholder="Placeholder"
                    class="description-input"
                    name="description"
                    maxlength="500"
                ></textarea>
            </div>
            <div class="form-container">
                <div class="until">
                    <!-- datapicker will be realised in a next task-->
                    <label class="until-title" for="until">Until</label>
                    <div class="until-container">
                        <input
                            class="until-input"
                            type="text"
                            name="until"
                            placeholder="12.05.2021"
                            maxlength="500"
                        />
                        <img
                            class="until-calendar"
                            alt="calendar"
                            src="/src/assets/images/card/calendar.svg
                        "
                        />
                    </div>
                </div>
                <div class="estimation">
                    <!-- datapicker will be realised in a next task-->
                    <label class="estimation-title" for="estimation"
                        >Estimation time</label
                    >
                    <div class="estimation-container">
                        <input
                            class="estimation-input"
                            type="text"
                            name="estimation"
                            placeholder="1h 30m"
                            maxlength="500"
                        />
                        <img
                            class="estimation-clock"
                            alt="clock"
                            src="/src/assets/images/card/clock.svg"
                        />
                    </div>
                </div>
                <div class="author">
                    <!-- choose author will be realised in a next task-->
                    <label class="author-title" for="author">Author</label>
                    <div class="author-container">
                        <input
                            class="author-input"
                            type="text"
                            name="author"
                            placeholder="Automatically"
                            maxlength="500"
                        />
                        <img
                            class="author-userpic"
                            alt="userpic"
                            src="/src/assets/images/card/userpic.svg"
                        />
                        <img
                            class="author-arrow"
                            alt="arrow"
                            src="/src/assets/images/card/choose-author.svg"
                        />
                    </div>
                </div>
            </div>
        </form>
        <div class="btn-container">
            <button type="submit" class="btn-create">Create task</button>
            <button type="button" class="btn-cancel" @click="$emit('close')">
                Cancel
            </button>
        </div>
    </div>
</template>

<style>
@import './CreateTaskForm.css';
</style>
