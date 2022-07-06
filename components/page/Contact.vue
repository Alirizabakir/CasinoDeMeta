<template>
    <Page id="contact" class="contact-box">
        <Container class="contact row">
            <div class="col">
                <div class="title">
                    <h2>
                        Casino De Meta Partners
                    </h2>
                    <p>
                        We are proud to be announce our professional partners soon.
                    </p>
                </div>
                <div class="form-box row">
                    <div class="col">
                        <div class="form row">
                            <form method="POST" class="col-md-6" action="submit">
                                <h2>
                                    Contact Us
                                </h2>
                                <div class="form-group">
                                    <label for="name"></label>
                                    <input id="name" type="text" placeholder="Your Name*">
                                </div>
                                <div class="form-group">
                                    <label for="email"></label>
                                    <input id="email" type="text" placeholder="Email Address*">
                                </div>
                                <div class="form-group">
                                    <label for="message"></label>
                                    <textarea id="message" style="resize: none;"
                                        placeholder="Write Message*"></textarea>
                                </div>
                                <div class="send row">
                                    <div class="col-md-6">
                                        reCAPTCHA
                                    </div>
                                    <div class="col-md-6">
                                        <button><img src="../../static/img/icons/send-icon.png" alt=""></button>
                                    </div>
                                </div>
                            </form>
                            <div class="col-md-6"></div>
                        </div>
                    </div>
                </div>

                <div class="subscribe-box">
                    <h3>
                        Don’t miss anything, Stay Connected
                    </h3>
                    <div class="subscribe row">
                        <div class="col-md-8">
                            <div class="row">
                                <input class="col-md-8" type="text" placeholder="Enter your Email address">
                                <button class="col-md-4">Subscribe</button>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="social-box row">
                    <div class="social col">
                        <a href="https://twitter.com/CasinoDeMeta" target="_blank">
                            <Twitter class="svg" />
                        </a>
                        <a href="https://www.telegram.com/" target="_blank">
                            <Telegram class="svg" />
                        </a>
                    </div>
                </div>
            </div>
        </Container>
    </Page>
</template>

<script>
import Page from '~/components/global/Page.vue';
import Container from '../global/Container.vue';
import Twitter from '../svg/Twitter.vue';
import Telegram from '../svg/Telegram.vue';
export default {
    name: "Contact",
    components: { Page, Container, Twitter, Telegram }
}
</script>

<style lang="scss" scoped>
.contact-box {
    background-color: #FFC71A;

    .contact {
        h2 {
            font-size: 36px;
            line-height: 70px;
            font-weight: 700;
            font-family: "glacial_indifferencebold";
        }

        .title {
            text-align: center;

            p {
                font-size: 16px;
            }
        }

        .form-box {
            box-shadow: 0px 15px 45px 0px rgb(0 0 0 / 25%);
            background-image: url(../../static/img/background/contact-section-bg.png);
            background-repeat: no-repeat;
            background-position: start;
            background-size: cover;
            border-radius: 10px;
            margin-top: 2rem;

            .form {
                form {
                    padding: 0 1rem;

                    border-right: none;

                    h2 {
                        margin-top: 20px;
                        margin-bottom: 10px;
                    }

                    input,
                    textarea {
                        width: 100%;
                        padding: 15px 0;
                        border: none;
                        background-color: transparent;
                        outline: none;
                        border-bottom: 1px solid #213284;
                        font-family: 'Poppins', sans-serif;
                    }

                    textarea {
                        height: 150px;
                    }

                    .form-group {
                        margin-bottom: 2rem;
                    }

                    .send {
                        margin-top: 20px;
                        margin-bottom: 10px;

                        div {
                            text-align: center;

                            button {
                                background-color: rgb(48, 79, 254);
                                padding: 10px;
                                border: none;
                                border-radius: 50%;
                                cursor: pointer;
                                transition: .3s;
                                margin: 1rem;

                                img {
                                    width: 15px;
                                    height: 15px;
                                }

                                &:hover {
                                    box-shadow: 0px 0px 5px rgb(48, 79, 254);
                                }
                            }
                        }
                    }
                }
            }
        }

        .subscribe-box {
            margin-top: 5rem;

            h3 {
                text-align: center;
                margin: 1rem 0;
                font-size: 20px;
                color: #000;
                font-family: 'Poppins', sans-serif;
                font-weight: 400;
            }

            .subscribe {
                div {
                    margin: 0 auto;

                    input {
                        border: 1px solid #3c3c3c;
                        outline: none;
                        padding: 20px 20px 20px 40px;
                        background: transparent;
                        font-size: 16px;
                        font-weight: 400;
                        color: #000;
                        margin-bottom: 1rem;
                    }

                    button {
                        border: 1px solid #3c3c3c;
                        font-size: 16px;
                        padding: 1rem;
                        color: #fff;
                        font-weight: 500;
                        outline: none;
                        background: #3c3c3c;
                        text-transform: capitalize;
                        margin-bottom: 1rem;

                    }
                }
            }
        }

        .social-box {
            .social {
                margin: 2rem auto;
                text-align: center;

                a {
                    margin: 1rem;
                    text-align: center;
                    width: 30px;
                    display: inline-block;
                    &:hover {
                        box-shadow: 0px 0px 4px white;
                    }
                    svg {
                        width: 100%;
                    }
                }
            }
        }
    }
}

@media screen and (min-width: 768px) {
    .contact-box {
        .contact {
            .form-box {
                .form {
                    form {
                        padding: 0 60px;
                        border-right: 1px solid #213284;

                        h2 {
                            margin-top: 80px;
                            margin-bottom: 50px;
                        }

                        textarea {
                            height: 200px;
                        }

                        .send {
                            margin-bottom: 80px;
                            margin-top: 50px;

                            div {
                                text-align: center;
                            }
                        }
                    }
                }
            }
        }
    }
}
</style>

