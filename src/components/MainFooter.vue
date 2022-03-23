<template>
    <footer>
        <div class="container">
            <Info />
            <Copyrights />
        </div>
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

footer {
    background-color: #202942;
    color: white;
}

</style>