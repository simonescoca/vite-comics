<template lang="">
    <section class="my_footer-links">
        <div class="container d-flex justify-content-between my_container">
            <div class="my_links d-flex">
                <div class="my_link1">
                    <h2>
                        DC Comics
                    </h2>
                    <ul class="list-unstyled">
                        <li v-for="element in navLinks">
                            <a href="#" class="my_footer-a">
                                {{element.text}}
                            </a>
                        </li>
                    </ul>
                    <h2>
                        SHOP
                    </h2>
                    <ul class="list-unstyled">
                        <li v-for="i in 2">
                            <a href="#" class="my_footer-a">
                                {{navLinks[i].text}}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="my_link2">
                    <h2>
                        DC
                    </h2>
                    <ul class="list-unstyled">
                        <li v-for="element in navLinks">
                            <a href="#" class="my_footer-a">
                                {{element.text}}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="my_link3">
                    <h2>
                        SITES
                    </h2>
                    <ul class="list-unstyled">
                        <li v-for="element in navLinks">
                            <a href="#" class="my_footer-a">
                                {{element.text}}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="my_bg-logo">
                <img :src="backgroundLogo.src" :alt="backgroundLogo.alt">
            </div>
        </div>
    </section>
    <section class="my_sign-up-and-social">
        <div class="container d-flex justify-content-between align-items-center my_sign-up-and-social-container">
            <div class="my_sign-up">
                <button type="button" class="btn btn-outline-primary">
                    Sign-Up NOW!
                </button>
            </div>
            <div class="d-flex justify-content-center align-items-center my_follow-us-container">
                <p class="m-0 my_follow-us">
                    FOLLOW US
                </p>
                <div class="d-flex align-items-center my_socials-images">
                    <img v-for="(image, index) in socialImages" :src="image.src" :alt="image.alt">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'AppFooter',
        data() {
            return {
                navLinks: [
                    {
                        text: "CHARACTERS",
                        active: false
                    },
                    {
                        text: "COMICS",
                        active: false
                    },
                    {
                        text: "MOVIES",
                        active: false
                    },
                    {
                        text: "TV",
                        active: false
                    },
                    {
                        text: "GAMES",
                        active: false
                    },
                    {
                        text: "COLLECTIBLES",
                        active: false
                    },
                    {
                        text: "VIDEOS",
                        active: false
                    },
                    {
                        text: "FANS",
                        active: false
                    },
                    {
                        text: "NEWS",
                        active: false
                    }
                ],

                backgroundLogo: {
                    src: "../../src/assets/img/dc-logo-bg.png",
                    alt: "logo di background"
                },

                socialImages: [
                    {
                        src: "../../src/assets/img/footer-facebook.png",
                        alt: "facebook logo"
                    },
                    {
                        src: "../../src/assets/img/footer-periscope.png",
                        alt: "periscope logo"
                    },
                    {
                        src: "../../src/assets/img/footer-pinterest.png",
                        alt: "pinterest logo"
                    },
                    {
                        src: "../../src/assets/img/footer-twitter.png",
                        alt: "twitter logo"
                    },
                    {
                        src: "../../src/assets/img/footer-youtube.png",
                        alt: "youtube logo"
                    }
                ]
            }
        },
    }
</script>

<style lang="scss" scoped>
    @use  "../styles/partials/variables";
    @use "../styles/partials/mixins";

    .my_container{
        padding: 2rem 0;
    }

    .my_footer-links {
        background-image: url("../assets/img/footer-bg.jpg");
        background-position: center;
        background-size: cover;
    }

    h2 {
        color: white;
    }

    .my_footer-a {
        color: #5f5f5f;
        font-size: .85rem;
        text-decoration: none;

        &:hover {
            color: white;
        }

    }

    .my_links {
        gap: 30px;
    }

    .my_sign-up-and-social {
        background-color: #303030;
    }

    .my_sign-up-and-social-container {
        padding: 1rem 0;
    }

    .my_follow-us-container {
        gap: 20px;
    }

    .my_follow-us {
        color: #0182f9;
        font-weight: 700;
        font-size: 2rem;
    }

    .my_socials-images {
        gap: 12px;
    }

    .my_bg-logo {
        height: 300px;
    }

    .my_bg-logo img {
        height: 100%;
        object-fit: cover;
        object-position: center;
    }

    .btn-outline-primary {
        color: white;
        border: 2px solid #0182f9;
        border-radius: 0;

        &:hover {
            background-color: #0182f9;
        }
    }
</style>