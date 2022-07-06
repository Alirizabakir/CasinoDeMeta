<template>
    <Page id="about" class="about">
        <Container class="box row">
            <section class="img-box col-md-6 px-0">
                <img src="../../static/img/pageimages/about/what-is-casino-de-meta.png" alt="">
            </section>
            <section class="text-box col-md-6 px-0">
                <h3>
                    What is Casino De Meta ?
                </h3>
                <p>
                    Casino De Meta is a blockchain structure that is based around casino games and lotteries. It
                    provides a fully transparent and a safe use to its users. Moreover, the users keep earning as long
                    as they keep playing within the system.
                </p>
                <p>
                    In addition to this they can take advantage of the jackpots that are within the games. Especially
                    the NFT marketplace that will be built within the casino can offer many suprise earnings to the
                    users.
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
    components: { Page, Container }
}
</script>

<style lang="scss" scoped>
.about {
    background: #ffc71a;
    padding-bottom: 5rem;
    
    .box {
        .text-box {
        padding-top: 3rem;

            text-align: center;

            h3 {
                font-family: 'glacial_indifferencebold';
                font-size: 36px;
            }

            p {
                margin: 30px 0;
                line-height: 30px;
            }
        }

        .img-box {
            text-align: center;
            img {
                width: 70%;
            }
        }
    }
}
@media screen and (min-width: 768px) {
    .about {

    .box {
        .text-box {
            text-align: left;

            h3 {
            }

            p {
            }
        }

        .img-box {
            text-align: left;

            img {
            }
        }
    }
}
}
</style>


