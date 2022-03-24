<!-- Questo componente raggruppa i principali componenti che formano l'header -->

<template>
    <header>
        <Navbar />
        <Jumbo />
        <Partners />
    </header>
</template>

<script>
import Navbar from './HeaderComponents/NavbarComponent.vue'
import Jumbo from './HeaderComponents/JumboComponent.vue'
import Partners from './HeaderComponents/PartnersComponent.vue'

export default {
    components: {
        Navbar,
        Jumbo,
        Partners,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/colorPalette.scss';

header {
    background-color: $headerBkg;
    // border-bottom: 1px solid black;
    // border-bottom-left-radius: 100px;
    // border-bottom-right-radius: 100px;
    // border-image: 30 round;
}
</style>