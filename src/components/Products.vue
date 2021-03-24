<template>
    <div class="container">
        <div class="products">
            <div class="title" v-html="title"></div>
            <div class="content">
                <div class="col-1">
                    <div class="product" v-for="product in products" :key="product.btnText">
                        <button
                                class="productBtn"
                                v-html="product.btnText"
                                :style="{
                                    border: `5px solid ${product.color}`,
                                    color: product.color
                                }"
                        />
                        <div class="productText" v-html="product.text"/>
                    </div>
                </div>
                <div class="col-2">
                    <img src="../assets/mobile.svg" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Products",
        data() {
            return {
                title: `Products`,
                products: [
                    {
                        btnText: `Launchpad`,
                        text: `Help launch startups & fund private bussinesses`,
                        color: `#252525`,
                    },
                    {
                        btnText: `Marketplace`,
                        text: `Browse through stocks on sale from private investors`,
                        color: `#2ECC71`
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    .container {
        width: 100%;
        margin: 0 auto;
    }

    .products {
        max-width: 1200px;
        padding: 59px 30px 0;
        min-height: 105px;
        margin: 0 auto;
    }

    .title {
        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 45px;
        line-height: 61px;
        color: #000000;
    }

    .content {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
    }

    .product {
        width: 350px;
        margin: 10px 0;
    }

    .col-1 {
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
    }

    .productBtn {
        width: 100%;
        height: 78px;
        background: none;
        border-radius: 10px;
        outline: none;

        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 32px;
        line-height: 44px;
        text-align: center;
    }

    .productText {
        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 22px;
        line-height: 30px;
        text-align: center;
        color: #000000;
    }
</style>