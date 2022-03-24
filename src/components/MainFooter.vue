<template>
    <footer>
        <Info />
        <Copyrights />
    </footer>
</template>

<script>
import Info from './FooterComponents/InfoComponent.vue'
import Copyrights from './FooterComponents/CopyrightsComponent.vue'

export default {
    components: {
        Info,
        Copyrights,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/colorPalette.scss';

footer {
    background-color: $footBkg;
    color: white;
    // position: relative;
}

</style>