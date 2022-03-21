<template>
    <div class="container">
        <Navbar />
        <Jumbo />
        <Partners />
    </div>
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

</style>