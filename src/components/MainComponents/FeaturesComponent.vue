<template>
    <section>
        <!-- questo componente è diviso in due righe: 
        - la prima è divisa in due colonne, di cui la prima contiene il titolo della sezione e il paragrafo, l'altra rimane vuota
        - la seconda contiene un v-for che ciclerà le card delle features -->

        <div class="col-2">
            <h2 class="section-title">Key Features</h2>
            <p class="section-decription">Start working with <span class="brand">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
        </div>

        <div id="featcard-wrapper" class="flex-row space-around">
            <div class="features-card" v-for="(feat, index) in features" :key="index">
                <div class="icon-wrapper">
                    <font-awesome-icon :icon="feat.icon" />
                </div>
                <h4>{{ feat.title }}</h4>
                <p>{{ feat.text }}</p>
                <a :href="feat.link">{{ feat.more }} <font-awesome-icon icon="fa-solid fa-chevron-right" /></a>
            </div>
        </div>

    </section>
</template>

<script>
export default {
    data() {
        return {
            features: [
                {
                    icon: 'fa-solid fa-database',
                    title: 'Modular',
                    text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Id, pariatur.',
                    link: '#',
                    more: 'Read more',
                },
                {
                    icon: 'fa-regular fa-square-caret-up',
                    title: 'Responsive',
                    text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Id, pariatur.',
                    link: '#',
                    more: 'Read more',
                },
                {
                    icon: 'fa-solid fa-jedi',
                    title: 'Customizable',
                    text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Id, pariatur.',
                    link: '#',
                    more: 'Read more',
                },
                {
                    icon: 'fa-solid fa-maximize',
                    title: 'Scalable',
                    text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Id, pariatur.',
                    link: '#',
                    more: 'Read more',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

#featcard-wrapper {
    gap: 15px;

    .features-card {
        padding: 15px;
        border: 1px solid #F5F6F7;
        border-radius: 5px;

        .icon-wrapper {
            background-color: #EAEEFB;
            border: none;
            color: #4F6FDB;
            padding: 3px;
            max-width: fit-content;
            font-size: 1.5rem;
            padding: 10px 15px;
            border-radius: 5px;
        }

        h4, p, a {
            margin: 15px 0;
            font-weight: 700;
        }

        p {
            color: #A6B0BE;
            font-size: 0.90rem;
        }

        a {
            color: #5877DC;

            .fa-chevron-right {
                font-size: 9px;
                vertical-align: middle;
            }
        }
    }
}
</style>