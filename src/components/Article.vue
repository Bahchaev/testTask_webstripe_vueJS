<template>
    <div class="container">
        <div class="article">
            <div class="title" v-html="title"></div>
            <div class="text" v-html="text"></div>
            <div class="cards">
                <Card
                        v-for="card in cards"
                        :image="card.image"
                        :title="card.title"
                        :text="card.text"
                        :key="card.title"
                />
            </div>
            <EmailForm/>

        </div>
    </div>
</template>

<script>
    import Card1 from '../assets/Card-1.svg'
    import Card2 from '../assets/Card-2.svg'
    import Card3 from '../assets/Card-3.svg'
    import Card from "@/components/Card";
    import EmailForm from "@/components/EmailForm";

    export default {
        name: "Article",
        components: {
            EmailForm,
            Card

        },
        data() {
            return {
                title: `What Are Digital Securities?`,
                text: `Digital securities represent traditional assets like equity or bonds. </br>
                They carry all of the same legal rights of their paper issued counter-parts.`,
                cards: [
                    {
                        image: Card1,
                        title: 'Invest Any Amount',
                        text: `Start with as little as $1, buy parts of a whole share`
                    },
                    {
                        image: Card2,
                        title: 'Access Private Equity',
                        text: `Get access to investments typically reserved for institutions`
                    },
                    {
                        image: Card3,
                        title: 'Trade 24/7',
                        text: `Digital assets don’t sleep, so why should you stop trading?`
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
        display: flex;
    }

    .article {
        max-width: 1200px;
        padding: 30px;
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
    }
     .title {
         font-family: Open Sans,sans-serif;
         font-style: normal;
         font-weight: 600;
         font-size: 45px;
         line-height: 61px;
         text-align: center;
         text-transform: capitalize;
         color: #000000;

         margin-bottom: 30px;
     }

    .text {
        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 25px;
        line-height: 34px;
        text-align: center;
        color: #000000;

        margin-bottom: 54px
    }

    .cards {
        display: flex;
        flex-wrap: wrap;
        flex-direction: row;
        justify-content: center;
        align-items: flex-end;
        margin-bottom: 26px;
    }

</style>