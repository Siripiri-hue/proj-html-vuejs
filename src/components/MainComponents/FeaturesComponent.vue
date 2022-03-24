<!-- 
Questo componente è diviso in due blocchi:
- il primo occupa il 50% dello spazio e contiene il titolo della sezione e relativo paragrafo 
- il secondo è il wrapper delle card, che contiene il v-for delle features
-->
        
<template>
    <section>
        <div class="col-2">
            <h2 class="section-title">Key Features</h2>
            <p class="section-description">Start working with <span class="brand">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
        </div>

        <div id="featcard-wrapper" class="flex-row space-around">
            <div class="features-card" v-for="(feat, index) in features" :key="index">
                <font-awesome-icon class="bg-icon" :icon="feat.icon" size="10x" />
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
@import '../../assets/scss/colorPalette.scss';

.col-2 {
    margin-bottom: 60px;
}

#featcard-wrapper {
    gap: 15px;

    .features-card {
        padding: 15px;
        border: 1px solid $cardBorder;
        border-radius: 5px;
        position: relative;
        overflow: hidden;
        width: calc(100% / 4);
        // flex-grow: 1;

        .icon-wrapper {
            background-color: $labelIcon;
            border: none;
            color: $LandrickViolet;
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
            color: $cardText;
            font-size: 0.90rem;
        }

        a {
            color: $linkColor;

            .fa-chevron-right {
                font-size: 9px;
                vertical-align: middle;
            }
        }

        .bg-icon {
            color: $iconBkg;
            position: absolute;
            right: -20px;
            top: 20%;
            z-index: -1;
            display: none;
        }

        &:hover {
            transform: translateY(-10px);

            .bg-icon {
                display: block;
            }
        }
    }
}
</style>