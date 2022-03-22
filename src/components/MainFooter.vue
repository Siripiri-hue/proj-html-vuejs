<template>
    <footer class="container">
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

</style>