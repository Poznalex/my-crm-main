<script setup></script>

<template>
    <div class="body">
        <div class="title">Create task</div>

        <section class="input-forms">
            <form class="name">
                <label class="name-title" for="name">Name</label>
                <input
                    type="text"
                    id="name"
                    name="name"
                    placeholder="Placeholder"
                    maxlength="500"
                />
            </form>

            <form class="description">
                <label class="description-title" for="name">Description</label>
                <input
                    type="text"
                    id="description"
                    name="name"
                    placeholder="Placeholder"
                    maxlength="500"
                />
            </form>

            <form class="until">
                <!-- datapicker will be realised in a next task-->
                <label class="until-title" for="name">Until</label>
                <input
                    type="text"
                    id="until"
                    name="name"
                    placeholder="Placeholder"
                    maxlength="500"
                />
            </form>

            <form class="estimation">
                <!-- datapicker will be realised in a next task-->
                <label class="estimation-title" for="name">Estimation time</label>
                <input
                    type="text"
                    id="estimation"
                    name="name"
                    placeholder="Placeholder"
                    maxlength="500"
                />
            </form>

            <form class="author">
                <!-- choose author will be realised in a next task-->
                <label class="author-title" for="name">Author</label>
                <input
                    type="text"
                    id="author"
                    name="name"
                    placeholder="Automatically"
                    maxlength="500"
                />
            </form>
        </section>

        <button type="button" class="btn-create">Create task</button>

        <button type="button" class="btn-cancel" @click="$emit('close')">Cancel</button>
    </div>
</template>

<style>
.body {
    display: flex;
    flex-direction: column;
    gap: 18px;
}

.title {
    font-size: 20px;
    font-weight: 700;
}

.input-forms {
    display: flex;
    flex-direction: column;
    gap: 12px;
    color: var(--main-color-grey);
}

label {
    font-size: 10px;
    font-weight: 600;
}

#until {
    background: url('/src/assets/images/card/calendar.svg') 98% center no-repeat;
    padding-right: 32px;
}

#estimation {
    background: url('/src/assets/images/card/clock.svg') 98% center no-repeat;
    padding-right: 32px;
}

#author {
    background: url('/src/assets/images/card/userpic.svg') 2% center no-repeat,
        url('/src/assets/images/card/arrow-down  choose author.svg') 95.5% center
            no-repeat;
    padding: 8px 32px;
}

#author::placeholder {
    color: var(--main-color-black);
}

.btn-create {
    background-color: var(--main-color-pink);
    font-size: 14px;
    color: var(--main-color-white);
    text-align: center;
    border-radius: 6px;
    padding: 6px;
    margin-top: 14px;
}

.btn-cancel {
    color: var(--main-color-light-blue);
    font-size: 14px;
    line-height: 10px;
}
</style>
