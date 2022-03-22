<template>
    <header>
        <div class="container">
            <Navbar />
            <Jumbo />
        </div>
        
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
header {
    background-color: #F8F9FC;
}
</style>