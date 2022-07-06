<template>
    <Page id="faq" class="faq-box">
        <Container class="faq">
            <div class="header">
                <h2>Frequently Asked Questions</h2>
                <p>FAQ</p>
            </div>

            <div class="row faq-list">
                <div class="list col-md-8 px-0">
                    <ul>
                        <li @click="open(index)" v-for="(item, index) in faqData" :key="index"
                            :class="{ animation: animate == index }">
                            <div>
                                <h2>{{ item.question }}</h2>
                                <span>
                                    <Up class="svg" />
                                </span>
                            </div>
                            <p>
                                {{ item.answer }}
                            </p>
                        </li>
                    </ul>
                </div>
            </div>
        </Container>
    </Page>
</template>

<script>
import Page from '@/components/global/Page.vue';
import Up from '@/components/svg/Up.vue';
export default {
    name: "Faq",
    components: { Page, Up },
    data() {
        return {
            animate: null,
            faqData: [
                {
                    question: '1. What makes Casino De Meta unique? ',
                    answer: 'While there are many online casinos, there are many factors that make Casino De Meta very \
                            unique. For example, the fact that it will be accessible from the metaverse makes it a \
                            very revolutionary concept. Moreover, rewards and advantages in our system are quite \
                            distinctive, too .'
                },
                {
                    question: '2. When will we be able to participate in games?',
                    answer: ' According to our road map, we will launch Casino De Meta in Q1 2023. So in near future, \
                                players will be able to participate in the games.'
                },
                {
                    question: '3. Which games will be playable in Casino De Meta?',
                    answer: 'Along with a unique system that we offer to our players and investors, we will have many \
                                games available in the Casino De Meta as well. To be specific, casino games such as \
                                roulette, blackjack, stud poker, Texas hold ‘em, punto banco and slot machines will be \
                                available in our casino.'
                },
                {
                    question: '4. How do you make money with Casino De Meta?',
                    answer: 'Basically a way to earn money in Casino De Meta, just like other casinos, is to \
                                participate in the games and win them. Also we offer many other ways to make money in \
                                this system. For instance, players who lose get CDM Token. Then investors can profit by \
                                staking in the system and get a percentage of the yearly revenue. So in Casino De Meta, \
                                there are many ways to earn.'
                },
                {
                    question: '5. How can I invest in this project?',
                    answer: ' Right now the project is in the development phase. However you can still invest in the \
                                project without losing any more time. Just purchase CDM Token and avoid missing out on \
                                this great offer.You can send email to investor@casinodemeta.com ,you will get detail \
                                information.'
                },
            ]
        }
    },
    methods: {
        open(index) {
            if (this.animate == index) {
                this.animate = null
            } else {
                this.animate = index
            }
        }
    },
}
</script>

<style lang="scss" scoped>
.faq-box {
    background-color: #fff;

    .faq {
        .header {
            text-align: center;

            h2 {
                color: #000;
                font-size: 22px;
                line-height: 40px;
                font-weight: 700;
                font-family: "glacial_indifferencebold";
            }

            p {
                margin: 1rem 0;

            }
        }
    }

    .faq-list {
        .list {
            margin: 0 auto;

            ul {
                li {
                    border: 1px solid black;
                    border-radius: 3px;
                    margin-bottom: 2rem;
                    cursor: pointer;
                    transition: .5s, background-color .2s;
                    max-height: 58px;
                    overflow: hidden;

                    div {
                        display: flex;
                        justify-content: space-between;
                        padding: 20px 35px;

                        h2 {
                            font-weight: 500;
                            font-size: 14px;
                            text-overflow: ellipsis;
                            white-space: nowrap;
                            overflow: hidden;
                            flex: 1;
                        }

                        span {
                            .svg {
                                width: 12px;
                                height: 12px;
                                transform: rotate(180deg);
                                padding: 0;
                                transition: .3s;
                                z-index: 10;
                            }
                        }
                    }

                    p {
                        padding: 0px 15px 24px 34px;
                        font-size: 14px;
                        line-height: 20px;
                    }
                }

                .animation {
                    background-color: #333;
                    color: #fff;
                    max-height: 400px;
                    transition: .5s, background-color 0s;

                    .svg {
                        transform: rotate(0deg);
                        fill: #fff;
                        transition: all .3s ease-in-out;

                    }
                }
            }
        }
    }
}

@media screen and (min-width: 768px) {
    .faq-box {
        background-color: #FFC71A;

        .faq {
            .header {
                text-align: center;

                h2 {
                    color: #000;
                    font-size: 36px;
                    line-height: 70px;
                    font-weight: 700;
                    font-family: "glacial_indifferencebold";
                }

                p {
                    margin: 1rem 0;

                }
            }
        }

        .faq-list {
            .list {

                ul {
                    li {

                        div {
                            padding: 20px 35px;

                            h2 {
                                font-size: 18px;
                                text-overflow: ellipsis;
                                white-space: nowrap;
                            }

                            .svg {
                                width: 12px;
                                height: 12px;
                                transform: rotate(180deg);
                                padding: 0;
                                transition: .3s;
                                z-index: 10;
                            }
                        }

                        p {
                            padding: 0px 15px 24px 34px;
                            font-size: 14px;
                            line-height: 20px;
                        }
                    }

                    .animation {
                        background-color: #333;
                        color: #fff;
                        max-height: 200px;
                        transition: .5s, background-color 0s;

                        .svg {
                            transform: rotate(0deg);
                            fill: #fff;
                            transition: all .3s ease-in-out;

                        }
                    }
                }
            }
        }
    }
}
</style>

