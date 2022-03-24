<!-- 
Questo componente contiene le icone dei partners
-->

<template>
    <section id="partners-row">
        <ul class="container flex-row space-around">
            <!-- v-for che cicla sull'array delle img dei loghi dei partner -->
            <li v-for="(partner, index) in partnersLogos" :key="index">
                <a :href="partner.link">
                    <img :src="partner.logo" alt="">
                </a>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    data() {
        return {
            partnersLogos: [
                {
                    logo: require('../../assets/img/amazon.svg'),
                    link: 'https://www.amazon.it/',
                },
                {
                    logo: require('../../assets/img/google.svg'),
                    link: 'https://www.google.it/',
                },
                {
                    logo: require('../../assets/img/lenovo.svg'),
                    link: 'https://www.lenovo.com/it/it/',
                },
                {
                    logo: require('../../assets/img/paypal.svg'),
                    link: 'https://www.paypal.com/it/home',
                }, 
                {
                    logo: require('../../assets/img/shopify.svg'),
                    link: 'https://it.shopify.com/',
                },
                {
                    logo: require('../../assets/img/spotify.svg'),
                    link: 'https://www.spotify.com/it/',
                },
            ],
        }
    }
    
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/colorPalette.scss';

#partners-row {
    border-top: 2px solid $headerLine;
    gap: 20px;
    padding: 40px 0 0;

    li {
        width: 70px;
    }
}

</style>