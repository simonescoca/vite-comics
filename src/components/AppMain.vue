<template lang="">
    <div class="my_main-background">
        <div class="container">
            <h1 class="my_main-content">
                --> Content here &lt;--
            </h1>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppMain',
        data() {
            return {
                
            }
        },
    }
</script>

<style lang="scss" scoped>
    @use  "../styles/partials/variables";
    @use "../styles/partials/mixins";

    .my_main-background {
        background-color: #1c1c1c;
        padding: 1rem 0;
    }

    .my_main-content {
        color: white;
        padding: .5rem 0;
    }

</style>