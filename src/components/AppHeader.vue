<template lang="">
    <header class="my_header">
        <section class="my_logo-sect">
            <img :src="logoIMG.src" :alt="logoIMG.alt">
        </section>
        <section class="my_links-sect">
            <ul>
                <li v-for="(element, index) in navLinks">
                    <a href="#">
                        {{navLinks[index]}}
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
                    src: "../assets/img/dc-logo.png",
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

        .my_logo-sect {

        }

        .my_links-sect {

        }
    }
</style>