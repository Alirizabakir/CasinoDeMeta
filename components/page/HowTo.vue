<template>
    <Page id="how-to" class="how-to">
        <Container class="box row">
            <section class="col-md-3">

            </section>
            <section class="text-box col-md-6">
                <h3>
                    How does the system work ?
                </h3>
                <p>
                    Aside from starting a very unique casino in the metaverse as Casino De Meta, our system is
                    well-designed and we offer many opportunities to our players and investors. Players will connect to
                    our system by linking their cryptocurrency wallet. Then you will be able to exchange certain coins
                    such as BTC, BNB and ETH to USDT, which you will be using for taking part in the games. On our
                    casino tables you will be able to play games such as; roulette, blackjack, stud poker, Texas hold
                    ‘em and slot machines.
                </p>
            </section>
            <section class="col-md-3">

            </section>
        </Container>
        <Container class="box-1 row">
            <section class="img-box col-md-4">
                <img src="../../static/img/pageimages/howto/139-.png" alt="">
                <h3>Create Account</h3>
                <p>
                    Register your Casino De <br>
                    Meta Account
                </p>
            </section>
            <section class="img-box col-md-4">
                <img src="../../static/img/pageimages/howto/556-.png" alt="">
                <h3>Open Wallet</h3>
                <p>
                    Open a new Casino De Meta <br>
                    Currency Wallet
                </p>
            </section>
            <section class="img-box col-md-4">
                <img src="../../static/img/pageimages/howto/402-.png" alt="">
                <h3>Send Receive Currency</h3>
                <p>
                    Start Reciving, Sending & <br>
                    exchanging Casino De Meta <br>
                    Currecy
                </p>
            </section>
        </Container>
        <Container class="box-2 row align-items-center">

            <section class="text-box col-md-6 px-0 pe-md-4">
                <h3>
                    Who we are?
                </h3>
                <p>
                    We are a professional team with our 30 year experience about landbase casinos including knowledge of
                    blockchain and high-tech ,offering you what you don’t know about casinos, instead of what you
                    already know.
                    <br> <br>
                    We are proud to be sharing our “new generation casino” idea with the investors in the industry. This
                    enterprise we are trying to bring into life will be one of the biggest changes in our field. The
                    advance of modern technology brought excitement to us as people who has been in the casino industry
                    for many years.
                </p>
            </section>

            <section class="img-box col-md-6 px-0">
                <div class="row">
                    <div class="col-md-4 d-flex flex-column justify-content-center align-items-center">
                        <div class="item">
                            <img src="../../static/img/pageimages/howto/shield.png" alt="">
                            <p>Secured <br> Payment</p>
                        </div>
                        <div class="item empty">
                        </div>
                    </div>
                    <div class="col-md-4 d-flex flex-column justify-content-center align-items-center">
                        <div class="item ">
                            <img src="../../static/img/pageimages/howto/mouse.png" alt="">
                            <p>One Click <br> Application</p>
                        </div>
                        <div class="item">
                            <img src="../../static/img/pageimages/howto/bill.png" alt="">
                            <p>Fully Secure</p>
                        </div>
                        <div class="item">
                            <img src="../../static/img/pageimages/howto/server.png" alt="">
                            <p>Internal <br> Integration</p>
                        </div>
                    </div>
                    <div class="col-md-4 d-flex flex-column justify-content-center align-items-center">
                        <div class="item">
                            <img src="../../static/img/pageimages/howto/control.png" alt="">
                            <p>External <br> Integration</p>
                        </div>
                        <div class="item">
                            <img src="../../static/img/pageimages/howto/payment.png" alt="">
                            <p>Payment <br> Getway</p>
                        </div>
                    </div>
                </div>
            </section>
        </Container>
        <Container class="box-3 row align-items-center">
            <section class="img-box col-md-6">
                <img src="../../static/img/pageimages/howto/benefits-of-using-our-system.png" alt="">
            </section>
            <section class="text-box col-md-6 px-0">
                <h3>
                    Benefits of using our system
                </h3>
                <p>
                    With Casino De Meta, players get to enjoy a wonderful casino experience in the Multiverse. Also with
                    our system, investors get access to a revolutionary way of profiting from the system
                    <br> <br>
                    Here with this system that we are putting in place, we are offering a brand new casino experience.
                    Moreover there are many benefits to using our solution.
                </p>
            </section>
        </Container>
    </Page>
</template>

<script>
import Page from '~/components/global/Page.vue';
import Container from '../global/Container.vue';
export default {
    name: "GlobalPageComponents",
    components: { Page, Container },
}
</script>

<style lang="scss" scoped>
.how-to {
    background: #ffc71a;
    padding-bottom: 5rem;

    .text-box {
        text-align: center;

        h3 {
            font-size: 36px;
            font-weight: 600;
        }

        p {
            margin: 30px 0;
            line-height: 30px;
        }

    }

    .box {
        text-align: center;
    }

    .box-1 {
        text-align: center;

        .img-box {
            margin-top: 4rem;

            h3 {
                font-size: 24px;
                color: #000;
                font-weight: 700;
                margin: 20px;
            }

            p {
                font-size: 16px;
                line-height: 30px;
                color: #000000;
            }

            img {
                background-color: #fff;
                padding: 20px;
                border-radius: 10px;
                width: 80px !important;
            }
        }
    }

    .box-2 {
        margin: 6rem 0;

        .img-box {
            text-align: center;

            .item {
                display: flex;
                align-items: center;
                justify-content: center;
                flex-direction: column;
                margin: 1rem 0;
                width: 280px;
                height: 280px;
                background-color: #fff;
                border-radius: 7px;
                transition: all .3s;

                img {
                    width: 35px;
                    margin-bottom: 20px;
                }

                p {
                    line-height: 20px;
                }
                &:hover {
                    transform: scale(1.03);
                }
            }

            .empty {
                display: none;
                background-color: transparent;
            }
        }
    }

    .box-3 {

        .img-box {
            text-align: center;
            margin-bottom: 2rem;

            img {
                width: 100%;
            }
        }
    }
}

@media screen and (min-width: 768px) {
    .how-to {
        .box-1 {
            .text-box {
                text-align: left;
            }
        }

        .box-2 {
            .text-box {
                text-align: left;
            }

            .img-box {
                .item {
                    width: 170px;
                    height: 180px;
                }

                .empty {
                    display: block;
                }
            }
        }

        .box-3 {

            .text-box {
                text-align: left;
            }

            .img-box {
                text-align: left;
                margin-bottom: 0;

                img {
                    width: 70%;
                }
            }
        }
    }
}
</style>


