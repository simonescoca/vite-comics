<template lang="">
        <header class="my_header">
            <div class="container d-flex align-items-center justify-content-between">
                <section class="my_logo-sect">
                    <img class="my_logo" :src="logoIMG.src" :alt="logoIMG.alt" />
                </section>
                <section class="d-flex align-items-center">
                    <ul class="d-flex align-items-center list-unstyled my_links-ul m-0">
                        <li v-for="(element, index) in navLinks">
                            <a href="#" :class="activeIndex === index ? 'my_active-li' : ''" @click="activeLi(index)">
                                {{element.text}}
                            </a>
                        </li>
                    </ul>
                </section>
            </div>
        </header>
</template>

<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
                activeIndex: undefined,
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
                    },
                    {
                        text: "SHOP",
                        active: false
                    }
                ],
                logoIMG: {
                    src: "../../src/assets/img/dc-logo.png",
                    alt: "DC Logo"
                }
            }
        },

        methods: {
            activeLi (index) {
                this.activeIndex = index
            }
        },
    }
</script>

<style lang="scss" scoped>
    @use  "../styles/partials/variables";
    @use "../styles/partials/mixins";

    .my_header {
        padding: 1rem 0;
    }

    .my_logo-sect {
        height: 50px;
    }

    .my_logo {
        height: 100%;
        object-fit: cover;
        object-position: center;
    }

    .my_links-ul {
        gap: 20px;
    }

    li a {
        text-decoration: none;
        color: black;

        &:hover {
            color: #0182f9;
        }
    }

    .my_active-li {
        color: #0182f9;
    }
</style>