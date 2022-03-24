<!-- Questo componente raggruppa i principali componenti che formano l'header -->

<template>
    <header>
        <div id="gear-icon"><font-awesome-icon icon="fa-solid fa-gear" /></div>

        <Navbar />
        <Jumbo />
    
        <!-- Partners escluso dal container per poter costruire la riga che separa i partners -->
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

    #gear-icon {
        position: absolute;
        top: 100px;
        left: 0;
        background-color: white;
        border-bottom-right-radius: 20px;
        border-top-right-radius: 20px;
        color: $blueBtn;
        padding: 7px;
    }
}
</style>