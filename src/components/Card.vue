<template>
    <div class="card">
        <img class="image" :src="image" alt="card">
        <div class="title" v-html="title"></div>
        <div class="text" v-html="text"></div>
    </div>
</template>

<script>
    export default {
        name: "Card",
        props: {
            image: Object,
            title: String,
            text: String
        }
    }
</script>

<style scoped>
    .card {
        max-width: 352px;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        align-items: center;
    }

    .image {
        margin-bottom: 30px;
    }

    .title {
        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 30px;
        line-height: 41px;
        text-align: center;
        color: #000000;

        margin-bottom: 17px;
    }

    .text {
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 22px;
        line-height: 30px;
        text-align: center;
        color: #000000;
    }
</style>