<template>
    <Page :class="{ scroll: scroll }" class="header-box">
        <div class="relative">
            <Container class="cont">
                <ul class="header row align-items-center my-4">
                    <li class="logo col-lg-2 col-4">
                        <img src="../../static/img/logo_white.png" alt="">
                    </li>
                    <li :class="{ active: isActive }" class="nav-box col-lg-10 px-0">
                        <ul class="nav-list row align-items-center justify-content-end">
                            <li @click="isActive = false" class="nav-item col-lg-1 px-0"
                                v-for="(item, index) in navigation" :key="index">
                                <a :href="`#${item.link}`">{{ item.title }}</a>
                            </li>
                            <li @click="isActive = false" :class="{ button: scroll }"
                                class="nav-item col-lg-3 px-0 route">
                                <a href="white">WHITEPAPER</a>
                            </li>
                        </ul>
                    </li>
                    <li @click="isActive = !isActive" :class="{ activeHamburger: scroll }" class="hamburger col-8">
                        <Hamburger v-show="!isActive" />
                        <Close v-show="isActive" />
                    </li>
                </ul>
            </Container>
        </div>
    </Page>
</template>

<script>
import Container from '../global/Container.vue'
import Hamburger from '../svg/Hamburger.vue'
import Page from '../global/Page.vue';
import Close from '../svg/Close.vue';

export default {
    components: { Container, Hamburger, Page, Close },

    data() {
        return {
            isActive: false,
            scroll: false,
            navigation: [
                {
                    title: "HOME",
                    link: "home"
                },
                {
                    title: "ABOUT",
                    link: "about"
                },
                {
                    title: "HOW TO",
                    link: "how-to"
                },
                {
                    title: "TOKEN",
                    link: "token"
                },
                {
                    title: "ROADMAP",
                    link: "road-map"
                },
                {
                    title: "FAQ",
                    link: "faq"
                },
                {
                    title: "CONTACT",
                    link: "contact"
                },
            ]
        };
    },
    methods: {
        // allpro(){
        //     this.$store.dispatch('allProductUpload', 'pro')
        // },

        handleScroll() {
            if (window.scrollY > 75) {
                this.scroll = true
            } else {
                this.scroll = false
            }
        },
    },
    created() {
        if (process.client) {
            window.addEventListener('scroll', this.handleScroll);
        }
    },
    destroyed() {
        if (process.client) {
            window.removeEventListener('scroll', this.handleScroll);
        }
    },
    mounted() {
        this.handleScroll()
    },
}
</script>

<style lang="scss" scoped>
.header-box {
    background-color: transparent !important;
    padding: 0 !important;
    position: sticky;
    top: 0;
    left: 0;
    right: 0;
    transition: all .4s;
    a {
        display: inline-block;
    }
    .relative {

        .cont {

            .header {

                .nav-box {
                    min-width: 100%;
                    position: absolute;
                    max-height: 0em;
                    top: 100%;
                    left: 0;
                    transition: all .3s;
                    overflow: hidden;
                    background-color: #F3F3F3;
                    padding: 0;


                    .nav-list {

                        .nav-item {
                            text-align: center;

                            a {
                                padding: 1rem 0;
                                color: #000;
                                font-weight: 400;
                                font-size: 14px;
                            }

                            &:hover {
                                a {
                                    color: #ffc71a;
                                }
                            }
                        }

                        .route {
                            a {
                                padding: 11px 32px;
                                background-color: #000;
                                color: #ffc71a;
                                border-radius: 5px;
                                letter-spacing: 1px;
                                font-weight: 600;

                                &:hover {
                                    box-shadow: 0px 0px 5px rgb(31, 39, 56);
                                    color: #F3F3F3;
                                }
                            }
                        }

                        .button {
                            a {
                                background-color: #ffc71a;
                                color: #000 !important;

                                &:hover {
                                    box-shadow: 0px 0px 5px rgb(255, 255, 255);
                                    color: #fff;
                                }
                            }
                        }
                    }


                }

                .active {
                    padding: 1rem 0;
                    max-height: 100vh !important;
                    box-shadow: 0px 3px 3px rgba(0, 0, 0, 0.535);
                    border-top: 1px solid black;
                }

                .hamburger {
                    text-align: right;
                    cursor: pointer;

                    svg {
                        width: 20px;
                        fill: #000;
                    }
                }

                .activeHamburger {
                    svg {
                        fill: #fff;
                    }
                }
            }
        }
    }
}

.scroll {
    background: #3f3f3f !important;

    .nav-box {
        background-color: #3f3f3f !important;

        .nav-list {


            .nav-item {
                a {
                    color: #fff !important;
                }
            }

            .route {
                a {
                    color: #ffc71a !important;
                }
            }
        }
    }

    .hamburger {
        svg {
            width: 20px;
            fill: #fff;
        }
    }
}

@media screen and (min-width: 992px) {
    .header-box {
        position: sticky;
        top: 0;
        transition: all .4s;

        .relative {
            .cont {

                .header {

                    .nav-box {
                        max-height: 100%;
                        min-width: auto;
                        position: static !important;
                        background-color: #F3F3F3;
                        transition: all .4s !important;
                        padding: 0 !important;

                        overflow: visible;

                        .nav-list {


                            .nav-item {
                                text-align: center;
                                padding: 1rem;

                                a {
                                    color: #000;
                                    font-weight: 500;
                                }
                            }

                            .route {
                                a {
                                    display: inline-block;
                                    padding: 11px 32px;
                                    background-color: #000;
                                    color: #ffc71a;
                                    border-radius: 5px;
                                    letter-spacing: 1px;
                                    font-weight: 600;
                                }
                            }

                            .button {
                                a {
                                    background-color: #ffc71a;
                                    color: #000 !important;
                                }
                            }
                        }


                    }

                    .active {
                        padding: 0;
                        max-height: 100vh;
                        box-shadow: none;
                        border-top: none;
                    }

                    .hamburger {
                        display: none;
                    }
                }
            }
        }
    }


}
</style>