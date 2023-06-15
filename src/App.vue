<template lang="">
    <div class="my_container">
        <AppHeader />
        <AppMain />
        <AppFooter />
    </div>
</template>

<script>
    // Descrizione:
    // Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
    // Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
    // Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!
    // Bonus:
    // Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.
    import AppHeader from "./components/AppHeader.vue"
    import AppMain from "./components/AppMain.vue"
    import AppFooter from "./components/AppFooter.vue"
    export default {
        components: {
            AppHeader,
            AppMain,
            AppFooter
        },

        data() {
            return {
                
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "./styles/general.scss";
</style>