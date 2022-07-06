<template>
    <Page class="home">
        <Container class="box row">
            <section class="img-box one col-md-6 px-0">
                <img src="../../static/img/pageimages/home/metaverse-casino-sharehodler.png" alt="">
            </section>
            <section class="text-box col-md-6 px-0">
                <h3>
                    Being a Metaverse Casino "ShareHodler"
                </h3>
                <p>
                    Best Unicorn crypto project in 2022 <br>
                    Las Vegas,Macau,Cyprus choose your Metaverse casino .. <br>
                    Top level of gameplay& investing… <br>
                    If you are investor of CDM token,you gonna be satisfied more then you think. <br>
                    Dividend for sharehodlers and Limited token supply <br>
                </p>
                <router-link to="/whitepaper/#">MORE</router-link>
            </section>
            <section class="img-box two col-md-6 px-0">
                <img src="../../static/img/pageimages/home/metaverse-casino-sharehodler-resize.png" alt="">
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
.home {
    background-image: url(../../static/img/background/dark.png);
    background-repeat: no-repeat;
    background-size: contain;
    background-position: bottom;
    padding-top: 4rem;
    padding-bottom: 4rem;
    background-color: #F3F3F3;
    .box {
        .text-box {
            padding-top: 5rem;
            text-align: center;

            h3 {
                font-family: 'glacial_indifferencebold';
                font-size: 30px;
            }

            p {
                margin: 30px 0;
                line-height: 34px;
                font-size: 14px;
            }

            a {
                font-size: 12px;
                color: #fff;
                display: inline-block;
                padding: 14px 30px;
                border: 1px solid #000;
                border-radius: 5px;
                letter-spacing: 3px;
                background-color: #000;
                &:hover {
                    color: #FFC71A;
                    box-shadow: 0px 0px 5px black;
                }
            }
        }

        .img-box {
            text-align: center;
            img {
                width: 80%;
            }
        }
        .one {
            display: block;
        }
        .two {
            display: none;
        }
    }
}

@media screen and (min-width: 768px) {
    .home {
    .box {
        .text-box {
            text-align: left;
        }

        .img-box {
            text-align: right;
        }

        .one {
            display: none;
        }
        .two {
            display: block;
        }
    }
}
}
</style>