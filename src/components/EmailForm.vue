<template>
    <form class="EmailForm" action="#">
        <input
                type="email"
                class="input"
                id="exampleInputPassword1"
                placeholder="E-mail"
        >
        <button
                type="submit"
                class="button"
        >Get Early Access
        </button>
    </form>
</template>

<script>
    export default {
        name: "EmailForm"
    }
</script>

<style scoped>

    .EmailForm {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .input {
        max-width: 445px;
        width: 100%;
        height: 47px;
        padding: 0 22px;
        margin: 15px;
        border: 1px solid #969696;
        box-sizing: border-box;
        border-radius: 10px;
        display: flex;
        outline: none;

        font-family: Open Sans,sans-serif;
        font-style: normal;
        font-weight: normal;
        font-size: 20px;
        line-height: 27px;
        color: black;
    }

    .input::placeholder {
        color: #969696;
    }

    .input:focus {
        border: 2px solid black;
    }

    .button {
        font-family: Open Sans, sans-serif;
        font-style: normal;
        font-weight: 600;
        font-size: 20px;
        line-height: 27px;
        text-align: center;
        color: #FFFFFF;


        min-width: 255px;
        height: 47px;
        background-color: #2ECC71;
        border-radius: 10px;
        border: none;
        outline: none;
        cursor: pointer;
        margin: 0 15px
    }

    .button:hover {
        text-decoration: underline;
        background-color: blue;
    }

    .button:active {
        transform: scale(0.9);
    }

    @media screen and (max-width: 767px) {
        .EmailForm {
            flex-wrap: wrap;
        }

        .input,
        .button {
            max-width: 445px;
            width: 100%;
        }


    }
</style>