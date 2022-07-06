<template>
    <Page class="footer-box">
        <Container class="footer row">
            <p class="col-md-7 px-0">Copyright @ 2022 Casino De Meta All Right Reserved.</p>
            <ul class="col-md-5 px-0 d-flex justify-content-between">
                <li>
                    <a href="https://casinodemeta.com">Home</a>
                </li>
                <li>
                    <a href="https://casinodemeta.com/whitepaper/index.php?slug=why-should-i-invest">Buy or Sell</a>
                </li>
                <li>
                    <a href="https://casinodemeta.com/privacy-policy">Privacy Policy</a>
                </li>
                <li>
                    <a href="https://casinodemeta.com/#faq">FAQ</a>
                </li>
                <li>
                    <a href="https://casinodemeta.com/contact">Contact</a>
                </li>
            </ul>
        </Container>
    </Page>
</template>

<script>
import Page from '~/components/global/Page.vue';
import Container from '~/components/global/Container.vue';

export default {
    components: { Page, Container, }
}
</script>

<style lang="scss" scoped>
.footer-box {
    background-color: #3c3c3c;
    padding: 2rem 0 !important;
    color: #fff;

    p {
        text-align: center;
        margin: 1rem 0;
        line-height: 20px;
    }

    ul {
        li {
                padding: 1rem 0;

            a {
                color: #fff;
                text-decoration: none;
                font-size: 11px;
                font-weight: 500;

                &:hover {
                    color: #FFC71A;

                }
            }
        }
    }
}

@media screen and (min-width: 768px) {
    .footer-box {
        padding: 4rem 0 !important;

        p {
            text-align: left;
        }

        ul {
            li {
                a {
                    color: #fff;
                    text-decoration: none;
                    font-size: 14px;
                    font-weight: 500;

                    &:hover {
                        color: #FFC71A;

                    }
                }
            }
        }
    }
}
</style>