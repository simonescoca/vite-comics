<template lang="">
    <div class="card">
        <img :src="propsCard.thumb" class="card-img-top" :alt="propsCard.type">
        <div class="card-body">
            <p class="card-text">
                {{propsCard.series}}
            </p>
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
            propsCard: Object
        },

        components: {

        }
    }
</script>

<style lang="scss" scoped>
    .card {
        width: 200px;
        height: 300px;
        background-color: transparent;
        --bs-card-border-width: 0;
    }

    .card-img-top {
        height: 200px;
        width: 100%;
        object-fit: cover;
        object-position: top;
    }

    .card-text {
        color: white;
        text-transform: uppercase;
    }
</style>