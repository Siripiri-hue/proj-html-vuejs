<template>
    <section id="tools" class="flex-row align-cx">
        <!-- componente diviso in due colonne:
        - la prima contiene il testo
        - la seconda contiene l'img -->

        <div class="col-2">
            <h2 class="section-title">Build tools and extensive documentation</h2>
            <p class="section-decription">You can combine all the Landrick templates into a single one, you can take a component from the Application theme and use it in a website</p>
            <button class="blue-btn">Read More <font-awesome-icon icon="fa-solid fa-arrow-right-long" /></button>
        </div>

        <div class="col-2">
            <img src="../../assets/img/1.png" alt="">
        </div>

    </section>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
.section-title {
    width: 65%;
}

</style>