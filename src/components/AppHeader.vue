<template lang="">
    <header class="my_header">
        <section class="my_logo-sect">
            <img class="my_logo" :src="logoIMG.src" :alt="logoIMG.alt" />
        </section>
        <section>
            <ul class="my_links-ul">
                <li v-for="(element, index) in navLinks">
                    <a href="#" @click="activeLi">
                        {{element.text}}
                    </a>
                </li>
            </ul>
        </section>
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
            activeLi (e) {
                this.activeIndex = index
                this.navLinks.active = true
                e.target.classList.add("my_active-li")
            }
        },
    }
</script>

<style lang="scss" scoped>
    @use  "../styles/partials/variables";
    @use "../styles/partials/mixins";

    .my_header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: .5rem 0;
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
        display: flex;
        align-items: center;
        gap: 20px;
        list-style: none;
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