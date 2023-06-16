<template lang="">
    <div class="my_jumbo-background">
        <!-- background -->
        <div class="my_current-series">
            CURRENT SERIES
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                
            }
        },

        props: {

        },

        components: {

        }
    }
</script>

<style lang="scss" scoped>
    .my_jumbo-background {
        background-image: url("../assets/img/jumbotron.jpg");
        background-position: top;
        background-size: cover;
        height: 500px;
        position: relative;
    }

    .my_current-series {
        background-color: #0182f9;
        padding: .5rem 1rem;
        position: absolute;
        bottom: -15px;
        left: 15%;
        color: white;
        font-weight: 700;
    }
</style>