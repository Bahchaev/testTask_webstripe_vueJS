<template>
    <div class="container">
        <div class="digitalAssets" v-html="text">

        </div>
    </div>
</template>

<script>
    export default {
        name: "DigitalAssets",
        data() {
            return {
                text: `Digital Assets are the future of private equity <br>
                - Deloitte`,
            }
        }
    }
</script>

<style scoped>
    .container {
        width: 100%;
        margin: 0 auto;
        background: #252525;
    }

    .digitalAssets {
        max-width: 920px;
        min-height: 181px;
        margin: 0 auto;
        padding: 0 30px;
        display: flex;
        align-items: center;
        justify-content: center;

        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 32px;
        line-height: 44px;
        text-align: center;
        color: #2FCC71;
    }

    @media screen  and (max-width: 768px){
        .digitalAssets {
            font-weight: normal;
            font-size: 22px;
            line-height: 30px;
        }
    }

</style>