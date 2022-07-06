<template>
    <Page id="road-map" class="roadmap-box">
        <Container class="roadmap d-flex flex-column align-items-center justify-content-center">
            <h2 class="mb-5 px-2">
                Casino De Meta Roadmap
            </h2>
            <img class="px-2" src="../../static/img/pageimages/roadmap/969-casino-de-meta-roadmap.png" alt="">
        </Container>
        <Container class="whitepaper row">
            <div class="title col-md-6 d-flex flex-column justify-content-center">
                <h2>Whitepaper</h2>
                <p>
                    In Casino De Meta project, we set the token allocation in a very reasonable manner. Basically, token
                    allocation means the allotment of tokens in this project, which you can buy or earn by winning games
                    in the casino system.
                    <br> <br>
                    Along with a reasonable token allocation, we also set the token vesting time in a very good manner
                    as well. Here are the graphs showing you how we will set the token allocation:
                </p>
                <div>
                    <router-link to="/whitepaper">SEE WHITEPAPER</router-link>
                </div>
            </div>
            <div class="img col-md-6">
                <img src="../../static/img/pageimages/roadmap/27596-whitepaper.png" alt="">
            </div>
        </Container>
        <Container class="team">
            <h2 class="header">
                Casino De Meta Team
            </h2>
            <div class="swiper">
                <!-- Additional required wrapper -->
                <div class="swiper-wrapper">
                    <!-- Slides -->
                    <div class="swiper-slide" v-for="(item, index) in teamData" :key="index">
                        <div class="img">
                            <img :src="require('../../static/img/pageimages/roadmap/' + item.img + '.jpg')" alt="">
                        </div>
                        <div class="info">
                            <h2>
                                {{ item.name }}
                            </h2>
                            <p>
                                {{ item.role }}
                            </p>
                        </div>
                    </div>
                </div>
                <!-- If we need pagination -->
                <div class="swiper-pagination d-flex align-items-center justify-content-center">
                    <span class="left move">
                        <Up class="svg" />
                    </span>
                    <span class="right move">
                        <Up class="svg" />
                    </span>
                </div>
            </div>
        </Container>
    </Page>
</template>

<script>
import Page from '~/components/global/Page.vue';
import Container from '../global/Container.vue';
import Up from '../svg/Up.vue';
export default {
    name: "Roadmap",
    components: { Page, Container, Up },
    data() {
        return {
            teamData: [
                {
                    name: 'Atıl Okay',
                    role: 'CASINO GENERAL MANAGER FOUNDER-CEO',
                    img: 'atil_oktay'
                },
                {
                    name: 'Hasan Leventyürü',
                    role: 'CASINO GENERAL MANAGER ADVISOR',
                    img: 'hasan_leventyuru'
                },
                {
                    name: 'Mehmet Öz',
                    role: 'CASINO GENERAL MANAGER ADVISOR',
                    img: 'mehmet_oz'
                },
                {
                    name: 'Uğurcan Alyüz',
                    role: 'FULL-STACK DEVELOPER',
                    img: 'ugurcan_alyuz'
                },
                {
                    name: 'Yuşa Baddal',
                    role: 'GAME DEVELOPER',
                    img: 'yusa_baddal'
                },
                {
                    name: 'Aylin Tekşen',
                    role: '3D ARTIST',
                    img: 'aylin_teksen'
                },
            ]
        }
    },
    mounted() {
        let span = document.getElementsByClassName('move');
        let product = document.getElementsByClassName('swiper-slide')
        let product_page = Math.ceil(product.length / 4);
        let l = 0;
        let movePer = 25.34;
        let maxMove = 75;
        // mobile_view	
        let mob_view = window.matchMedia("(max-width: 768px)");
        if (mob_view.matches) {
            movePer = 100;
            maxMove = 504;
        }

        let right_mover = () => {
            l = l + movePer;
            if (product == 1) { l = 0; }
            for (const i of product) {
                if (l > maxMove) { l = l - movePer; }
                i.style.left = '-' + l + '%';
            }

        }
        let left_mover = () => {
            l = l - movePer;
            if (l <= 0) { l = 0; }
            for (const i of product) {
                if (product_page > 1) {
                    i.style.left = '-' + l + '%';
                }
            }
        }
        span[1].onclick = () => { right_mover(); }
        span[0].onclick = () => { left_mover(); }
    },
}
</script>

<style lang="scss" scoped>
.roadmap-box {
    background-color: #FFC71A;

    .roadmap {
        padding: 0 !important;

        h2 {
            text-align: center;
            font-size: 34px;
            font-weight: 700;
        }

        img {
            width: 100%;
        }
    }

    .whitepaper {
        padding: 4rem 0;

        .title {
            text-align: center;

            h2 {
                font-size: 34px;
                font-weight: 700;
            }

            p {

                font-size: 14px;
                margin: 2rem 0;
                line-height: 30px;
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
                transition: all .3s;

                &:hover {
                    box-shadow: 0px 0px 4px #000000;
                    color: #ffc71a;
                }
            }
        }

        .img {
            margin-top: 2rem;

            img {
                width: 100%;
            }
        }
    }

    .team {
        .header {
            text-align: center;
            margin: 4rem 0;
            font-size: 36px;
            font-weight: 700;
            font-family: "glacial_indifferencebold";
        }

        .swiper {
            .swiper-wrapper {
                width: 100%;
                height: 400px;
                /*background: red;*/
                display: flex;
                align-items: center;
                overflow-x: auto;

                &::-webkit-scrollbar {
                    display: none;
                }

                .swiper-slide {
                    text-align: center;
                    min-width: 100%;
                    padding: 0;
                    height: 90%;
                    position: relative;
                    left: 0;
                    transition: 0.5s;
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;

                    .img {
                        width: 100%;
                        height: 80%;
                        border-radius: 10px;

                        img {
                            border-radius: 20px;
                            width: auto;
                            max-height: 100%;
                        }
                    }

                    .info {
                        margin-top: 1rem;

                        h2 {
                            font-size: 20px;
                            font-weight: 600;
                            font-family: "glacial_indifferencebold";
                        }

                        p {
                            font-size: 14px;
                            font-weight: normal;
                            line-height: 24px;
                            width: 70%;
                            margin: 0 auto;
                        }
                    }
                }
            }

            .swiper-pagination {

                .left,
                .right {
                    text-align: center;
                    border: 1px solid black;
                    border-radius: 50%;
                    margin: 1rem;

                    .svg {
                        text-align: center;
                        width: 15px;
                        height: 15px;
                        margin: 5px;
                    }
                }

                .move {
                    cursor: pointer;

                    &:hover {
                        background-color: #000;

                        .svg {
                            fill: #FFC71A;
                        }
                    }
                }

                .left {
                    transform: rotate(-90deg);
                }

                .right {
                    transform: rotate(90deg);
                }
            }
        }
    }
}

@media screen and (min-width: 768px) {
    .roadmap-box {
        background-color: #FFC71A;

        .roadmap {
            padding: 0 !important;

            h2 {
                text-align: center;
                font-size: 34px;
                font-weight: 700;
            }


            img {
                width: 50%;
            }
        }

        .whitepaper {

            .title {
                text-align: left;

                h2 {
                    font-size: 34px;
                    font-weight: 700;
                }

                a {
                    font-size: 12px;
                }
            }

            .img {
                margin-top: 0;

                img {
                    width: 70%;
                    float: right;
                }
            }

        }

        .swiper {

            .swiper-wrapper {
                .swiper-slide {
                    min-width: 25% !important;
                    padding: 0 .5rem !important;
                }
            }
        }
    }
}
</style>

