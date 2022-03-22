<template>
    <main class="container">
        <Features />
        <Quickstart />
        <Tools />
        <Rates />
        <Cta />
    </main>
</template>

<script>
import Features from './MainComponents/FeaturesComponent.vue'
import Quickstart from './MainComponents/QuickstartComponent.vue'
import Tools from './MainComponents/ToolsComponent.vue'
import Rates from './MainComponents/RatesComponent.vue'
import Cta from './MainComponents/CtaComponent.vue'

export default {
    components: {
        Features,
        Quickstart,
        Tools,
        Rates,
        Cta,
    }
}
</script>

<style lang="scss" scoped>

</style>