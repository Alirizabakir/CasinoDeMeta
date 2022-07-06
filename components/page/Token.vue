<template>
    <Page id="token" class="token">
        <Container class="count-down-box px-lg-0 px-2">
            <div class="padd row">
                <div class="count-down col-lg-8 px-0 col d-flex flex-column align-items-center justify-content-center">
                    <h2>
                        COUNTDOWN
                    </h2>
                    <div class="count-box">
                        <div class="count">
                            <div class="item days">
                                <div class="num">
                                    <span v-show="days.toString().length < 2">0</span>
                                    <span>{{ days }}</span>
                                </div>
                                <p>DAYS</p>
                            </div>
                            <div class="item hour">
                                <div class="num">
                                    <span v-show="hours.toString().length < 2">0</span>
                                    <span>{{ hours }}</span>
                                </div>
                                <p>HOUR</p>
                            </div>
                            <div class="item min">
                                <div class="num">
                                    <span v-show="mins.toString().length < 2">0</span>
                                    <span>{{ mins }}</span>
                                </div>
                                <p>MINS</p>
                            </div>
                            <div class="item sec">
                                <div class="num">
                                    <span v-show="secs.toString().length < 2">0</span>
                                    <span>{{ secs }}</span>
                                </div>
                                <p>SEC</p>
                            </div>
                        </div>
                    </div>
                    <div class="payment d-flex flex-column flex-md-row justify-content-between align-items-center ">
                        <div>
                            <img src="../../static/img/pageimages/token/payment-icon.png" alt="">
                        </div>
                        <div class="button">
                            <a href="mailto:investor@casinodemeta.com">INVEST</a>
                        </div>
                    </div>
                </div>
            </div>
        </Container>
        <Container class="title row">
            <div class="sale">
                <h2>
                    Private Token Sale
                </h2>
                <div class="row">
                    <div class="col-md-2 px-0">

                    </div>
                    <p class="col-md-4">
                        Start Time : 1st July 2022 (09:00) GMT +03:00 <br> <br>
                        Hard Caps : 5 M USD <br> <br>
                        Available Token :18 M USD <br> <br>
                    </p>
                    <p class="col-md-4">
                        End Time :1st July 2022 (09:00) GMT +03:00 <br> <br>
                        Soft Caps : None <br> <br>
                        Acceptable Currency :BTC,ETH,USDT,USDC,BUSD <br> <br>
                    </p>
                    <div class="col-md-2 px-0">

                    </div>
                </div>
            </div>
            <div class="hodlers">
                <h2>
                    Benefits for Token Hodlers
                </h2>
                <p>
                    With Casino De Meta, players get to enjoy a wonderful casino <br>experience in the Multiverse
                </p>
            </div>
        </Container>
        <Container class="row feature">
            <div class="col-md-4">
                <img src="../../static/img/pageimages/token/172-staking-rewards.png" alt="">
                <h3>Staking Rewards</h3>
                <p>Investors will receive annual dividends according to their yearly stakings with legally approved
                    special agreement. This investing opportunity is the only one of its kind and the best one in
                    market.</p>
            </div>
            <div class="col-md-4">
                <img src="../../static/img/pageimages/token/179-efficient-work.png" alt="">
                <h3>Efficient Work
                </h3>
                <p>Casino De Meta is designed to be a cross-chain protocol to optimize smart contracts costs and
                    transactions fees. The protocol's unique approach allows it to provide an efficient user experience.

                </p>
            </div>
            <div class="col-md-4">
                <img src="../../static/img/pageimages/token/404-full-transparency.png" alt="">
                <h3>Full Transparency
                </h3>
                <p>In order to provide full transparency to its users, Casino De Meta runs over multiple smart contracts
                    on decentralized blockchains. Shareholders, players and liquidity providers get access to all the
                    data what they need.

                </p>
            </div>
            <div class="col-md-4">
                <img src="../../static/img/pageimages/token/371-community-governance.png" alt="">
                <h3>Community Governance
                </h3>
                <p>Platform is community-driven. As a token holder, you will play a critical role in each evolution,
                    proposal, decision, and everything in between. We will work together and combine our ideas to
                    generate the best outcome.

                </p>
            </div>
            <div class="col-md-4">
                <img src="../../static/img/pageimages/token/216-a-completely-new-casino-experience.png" alt="">
                <h3>A Completely New Casino Experience
                </h3>
                <p>Casino De Meta revolutionizes the casino experience by offering a brand new system that works in the
                    Metaverse. Here in this system players get to enjoy a transparent casino experience while investors
                    get access to a new earning method.

                </p>
            </div>
            <div class="col-md-4">
                <img src="../../static/img/pageimages/token/412-find-all-in-one-app.png" alt="">
                <h3>Find All in One App
                </h3>
                <p>Users can find everything that they need in the all-in-one app that provides a vibrant and
                    entertaining gaming experience. Its streamlined interface gives users easy access to their favorite
                    games, pools and wallet.

                </p>
            </div>
        </Container>
        <div class="tokenomics">
            <Container class="content">
                <h2 class="py-2">TOKENOMICS</h2>
                <div class="row">
                    <div class="col-md my-5 px-0">
                        <h3>Token Distribution</h3>
                        <img src="../../static/img/pageimages/token/455-token.png" alt="">
                    </div>
                    <div class="col-md my-5 px-0">
                        <h3>Token Realese Schedule-Vesting</h3>
                        <img src="../../static/img/pageimages/token/493-token-distribution-vesting.png" alt="">
                    </div>
                </div>
            </Container>
        </div>
    </Page>
</template>

<script>
import Page from '~/components/global/Page.vue';
import Container from '../global/Container.vue';
export default {
    name: "Token",
    components: { Page, Container },
    data() {
        return {
            days: 0,
            hours: 0,
            mins: 0,
            secs: 0,
        }
    },
    methods: {
        countDown() {
            setInterval(() => {
                const nowTime = new Date().getTime()
                const countTime = new Date('Sun Jul 25 2022 00:00:00 GMT+0300').getTime()
                const gap = countTime - nowTime

                const sec = 1000
                const min = sec * 60
                const hour = min * 60
                const day = hour * 24

                this.days = Math.floor(gap / day)
                this.hours = Math.floor((gap % day) / hour)
                this.mins = Math.floor((gap % hour) / min)
                this.secs = Math.floor((gap % min) / sec)
            }, 1000);
        }
    },
    mounted() {
        this.countDown()
    },
}
</script>

<style lang="scss" scoped>
.token {
    h2 {
        font-weight: 700;
        font-family: "glacial_indifferencebold";
    }

    .count-down-box {
        .padd {
            background-color: #fafafa40;
            border-radius: 5px;
            height: auto;
            padding: 2rem !important;
            width: 100%;
            margin: 0;

            .count-down {
                margin: 0 auto;
                height: auto;

                h2 {
                    font-size: 36px;
                    color: #000;
                    text-transform: uppercase;
                    letter-spacing: 3px;
                    font-family: 'glacial_indifferenceregular';
                    text-align: center;
                }

                .count-box {
                    border: 1px solid black;
                    border-radius: 5px;
                    margin: 2rem 0;
                    padding: 2rem 0;
                    width: 100%;

                    .count {
                        display: grid;
                        grid-template-columns: repeat(4, 1fr);

                        .item {
                            text-align: center;

                            .num {
                                font-size: 18px;
                                font-weight: 700;
                                display: flex;
                                justify-content: center;
                                font-family: 'glacial_indifferencebold';
                            }

                            p {
                                color: #000000;
                                font-family: 'Poppins', sans-serif;
                                font-weight: 400;
                                letter-spacing: 2px;
                                font-size: 10px;
                            }
                        }
                    }
                }

                .payment {
                    width: 100%;

                    .button {
                        margin-top: 2rem;



                        a {
                            display: inline-block;
                            padding: 15px 40px;
                            font-size: 12px;
                            border-radius: 5px;
                            color: #fff;
                            border: none;
                            letter-spacing: 2px;
                            -webkit-transition: all .3s ease-out;
                            transition: all .3s ease-out;
                            font-weight: 500;
                            background-color: #3c3c3c;

                            &:hover {
                                box-shadow: 0px 0px 4px #000000;
                                color: #ffc71a;
                            }
                        }
                    }
                }
            }
        }
    }

    .title {
        padding: 6rem 0 !important;

        .sale {
            margin: 5rem 0;

            h2 {
                text-align: center;
                font-size: 36px;
            }

            p {
                margin-top: 2rem;
                font-weight: 500;
            }
        }

        .hodlers {
            padding: 5rem 0;

            h2 {
                text-align: center;
                font-size: 36px;
                margin: 1rem 0;

            }

            p {
                text-align: center;
                line-height: 30px;
            }
        }
    }

    .feature {
        padding: 0 !important;

        div {
            margin: 2rem 0;

            img {
                width: 55px;
            }

            h3 {
                margin: 1rem 0;
                font-size: 20px;
            }

            p {
                line-height: 30px;
            }
        }
    }

    .tokenomics {
        background-image: url(../../static/img/background/small-top.png), url(../../static/img/background/small-bottom.png);
        background-position: top, bottom;
        background-repeat: no-repeat, no-repeat;
        background-size: 100% auto;
        background-color: white;
        padding: 4rem 0;

        .content {
            h2 {
                text-align: center;
                font-size: 36px;
            }

            h3 {
                text-align: center;
                font-size: 25px;
                font-weight: 500;
                margin: 2rem 0;
            }
        }
    }

}

@media screen and (min-width: 768px) {
    .token {
        padding: 0;

        .count-down-box {

            .count-down {
                height: 55vh !important;

                .count-box {
                    margin: 3rem 0;
                    padding: 3rem;

                    .count {
                        .item {
                            .num {
                                font-size: 48px !important;
                                font-weight: 700;
                            }

                            p {
                                font-size: 14px;
                            }
                        }
                    }
                }

                .payment {
                    .button {
                        margin-top: 0rem !important;
                    }
                }
            }
        }

        .tokenomics {
            padding: 13rem 0;

            .content {
                h3 {
                    font-size: 30px;
                }
            }
        }


    }
}
</style>

