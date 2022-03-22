<template>
    <section id="partners-row" class="container">
        <!-- v-for che cicla sull'array delle img dei loghi dei partner -->
        <ul class="flex-row space-around">
            <template v-for="(partner, index) in partnersLogos">
                <li :key="index">
                    <a :href="partner.link">
                        <img :src="partner.logo" alt="">
                    </a>
                </li>
            </template>
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

#partners-row {
    border-top: 2px solid #ebeef1;
    gap: 20px;
    padding: 40px 0;

    li {
        width: 70px;
    }
}

</style>