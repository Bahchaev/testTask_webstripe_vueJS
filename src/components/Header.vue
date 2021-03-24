<template>
    <div class="container">
        <div class="header">
            <div class="content">
                <div class="title">{{title}}</div>
                <div class="wrapper">
                    <div class="text">{{text}}</div>
                    <button class="button">{{buttonText}}</button>
                </div>
            </div>
            <img :src="image" alt="image" class="image">
        </div>
    </div>
</template>

<script>
    import image from '../assets/mobile-header.svg'
    export default {
        name: "Header",

        data() {
            return {
                title: 'Private Equity Made Easy',
                text: `Equiteez is on a mission to make private
                    equity easily accesible to all in vestors`,
                buttonText: `Singnup For Free`,
                image: image

            }
        }
    }
</script>

<style scoped>

    .container {
        width: 100%;
        margin: 0 auto;
        display: flex;
        background: #2ECC71;
        overflow: hidden;
    }

    .header {
        max-width: 1200px;
        padding: 30px;
        min-height: 769px;
        margin: 0 auto;
        display: flex;
        position: relative;
    }

    .content {
        width: 55%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        z-index: 1;
    }

    .title {
        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: bold;
        font-size: 52px;
        line-height: 71px;
        color: #FFFFFF;

        margin-bottom: 28px;
    }

    .text {
        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 32px;
        line-height: 44px;
        color: #FFFFFF;

        margin-bottom: 39px;
    }

    .button {
        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 20px;
        line-height: 27px;
        text-align: center;

        display: block;
        color: #FFFFFF;
        width: 255px;
        height: 56px;
        background: #252525;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
        border-radius: 10px;
        border: none;
        outline: none;
        cursor: pointer;
    }

    .button:hover {
        text-decoration: underline;
        background: dimgray;
    }

    .button:active {
        transform: scale(0.9);
    }

    .image {
        position: absolute;
        right: -200px;
        top: -35px;
    }

        @media screen and (max-width: 767px) {
        .content {
            width: 100%;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
        }

        .title {
            font-size: 35px;
            line-height: 40px;
            text-align: center;
        }

        .text {
            font-weight: 600;
            font-size: 22px;
            line-height: 25px;
            text-align: center;
        }

        .button {
            margin: 0 auto;
        }

        .image {
            height: 644px;
            width: 625px;
            top: 10px;
        }
    }

</style>