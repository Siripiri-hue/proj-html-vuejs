<template>
    <section id="tools" class="flex-row align-cx">
        <!-- componente diviso in due colonne:
        - la prima contiene il testo
        - la seconda contiene l'img -->

        <div class="col-2">
            <h2 class="section-title">Build tools and extensive documentation</h2>
            <p class="section-description">You can combine all the Landrick templates into a single one, you can take a component from the Application theme and use it in a website</p>

            <div class="section-description flex-col">
                <span v-for="(tool, index) in tools" :key="index">
                    <font-awesome-icon icon="fa-regular fa-circle-check" class="blue-text" /> {{ tool }}
                </span>
            </div>

            <button class="blue-btn">Read More <font-awesome-icon icon="fa-solid fa-arrow-right-long" /></button>
        </div>

        <div class="col-2">
            <img src="../../assets/img/1.png" alt="">
        </div>

    </section>
</template>

<script>
export default {
    data() {
        return {
            tools: ['Digital Marketing Solutions for Tomorrow', 'Our talented & experienced Marketing Agency', 'Create you own skin to match your brand'],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/colorPalette.scss';

.section-title {
    width: 65%;
}

span .blue-text {
    padding-right: 5px;
}

// hover button
button:hover {
    box-shadow: 0px 4px 5px -2px $btnsShadow;
}

.col-2:last-child {
    padding: 40px;
}

</style>