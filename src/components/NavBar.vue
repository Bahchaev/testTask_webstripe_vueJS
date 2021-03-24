<template>
    <div class="container">
        <div class="navBar">
            <span class="expandBtn" v-on:click="btnHandleClick">
                <span class="toggler-rect"/>
                <span class="toggler-rect"/>
                <span class="toggler-rect"/>
            </span>
            <img :src="logo.src" alt="logo" class="logo">
            <div class="links-wrap" v-if="isExpanded === false ? true : isShown">
                <div class="links">
                    <a v-for="link in navLinks" :key="link.text" :href="link.href">
                        {{link.text}}
                    </a>
                </div>
                <div class="socLinks">
                    <a v-for="link in socLinks" :key="link.href" :href="link.href">
                        <img v-bind:src="link.src" alt="logo">
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import logo from '../assets/Equiteez.svg'
    import facebookIcon from '../assets/Facebook.svg'
    import twitterIcon from '../assets/Twitter.svg'
    import linkedinIcon from '../assets/Linkedin.svg'
    import mediumIcon from '../assets/Medium.svg'

    export default {
        name: 'NavBar',
        props: {
            msg: String
        },
        data() {
            return {
                logo: {
                    src: logo
                },
                navLinks: [
                    {
                        text: 'What Are Digital Securities?',
                        href: '#WhatAreDigitalSecurities'
                    },
                    {
                        text: 'Products',
                        href: '#Products'
                    },
                    {
                        text: 'Digitize Your Business',
                        href: '#'
                    },
                    {
                        text: 'Blog',
                        href: '#'
                    },
                    {
                        text: 'Contact Us',
                        href: '#'
                    }
                ],
                socLinks: [
                    {
                        href: "https://twitter.com/",
                        src: twitterIcon
                    },
                    {
                        href: "https://www.facebook.com/",
                        src: facebookIcon
                    },
                    {
                        href: "https://ru.linkedin.com/",
                        src: linkedinIcon
                    },
                    {
                        href: "https://medium.com/",
                        src: mediumIcon
                    }
                ],

                isShown: false,
                isExpanded: false
            }
        },
        methods: {
            btnHandleClick: function () {
                console.log(this.isShown);
                this.isShown = !this.isShown;
            },
            setIsExpanded() {
                this.isExpanded = window.innerWidth < 1200;
            }
        },
        created() {
            window.addEventListener('resize', this.setIsExpanded);
            this.setIsExpanded()
        }

    }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

    .container {
        width: 100%;
        margin: 0 auto;
    }

    .navBar {
        max-width: 1200px;
        padding: 0 30px;
        min-height: 105px;
        margin: 0 auto;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        flex-wrap: nowrap;
        position: relative;
        transition: height 5s;
    }

    .expandBtn {
        border: none;
        position: absolute;
        left: 30px;
        top: 33px;
        height: 38px;
        background: none !important;
        display: none;
        justify-content: space-evenly;
        align-items: center;
        flex-direction: column;

    }

    .toggler-rect {
        height: 4px;
        width: 30px;
        background-color: #2ECC71;
    }

    .links-wrap {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .links {
        display: flex;
        justify-content: flex-start;
    }

    .logo {
        width: 179px;
        height: 51px;
        margin-right: 24px;;
    }

    a,
    a:active,
    a:visited {
        text-decoration: none;
    }

    .links a {
        font-family: Open Sans, serif;
        font-style: normal;
        font-weight: 600;
        font-size: 18px;
        line-height: 25px;
        color: #000000;

        margin-right: 22px;
        padding: 8px 0;
    }

    .socLinks {
        padding: 8px 0;
    }

    .links a:hover {
        text-decoration: underline;
    }

    .links a:active {
        font-weight: 900;
    }

    .socLinks a:not(:last-child) {
        margin-right: 7px;
    }

    @media screen and (max-width: 1200px) {
        .logo {
            margin-top: 27px;
        }

        .navBar,
        .links-wrap,
        .links {
            flex-direction: column;
        }

        .links-wrap,
        .links {
            align-items: flex-start;
        }

        .expandBtn {
            display: flex;
        }
    }
</style>
