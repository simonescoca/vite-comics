<template lang="">
    <header class="my_header">
        <section class="my_logo-sect">
            <img class="my_logo" :src="logoIMG.src" :alt="logoIMG.alt" />
        </section>
        <section>
            <ul class="my_links-ul">
                <li v-for="element in navLinks">
                    <a href="#">
                        {{element}}
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
                navLinks: ["CHARACTERS", "COMICS", "MOVIES", "TV", "GAMES", "COLLECTIBLES", "VIDEOS", "FANS", "NEWS", "SHOP"],
                logoIMG: {
                    src: "../../src/assets/img/dc-logo.png",
                    alt: "DC Logo"
                }
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

        .my_logo-sect {
            height: 50px;

            .my_logo {
                height: 100%;
                object-fit: cover;
                object-position: center;
            }
        }

        .my_links-ul {
            display: flex;
            align-items: center;
            gap: 20px;
            list-style: none;

            li a {
                text-decoration: none;
                color: black;

                &:hover {
                    color: red;
                }
            }
        }
    }
</style>