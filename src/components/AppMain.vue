<template lang="">
    <div>
        <JumboComponent />
        <SeriesComponent />
    </div>
</template>

<script>
    import JumboComponent from "./JumboComponent.vue"
    import SeriesComponent from "./SeriesComponent.vue"
    export default {
        name: 'AppMain',

        components: {
            JumboComponent,
            SeriesComponent
        },

        data() {
            return {

            }
        },
    }
</script>

<style lang="scss" scoped>
    @use  "../styles/partials/variables";
    @use "../styles/partials/mixins";
</style>