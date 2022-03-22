<template>
    <ul id="partners-row" class="flex-row just-cx">
        <!-- qui metterò un v-for che ciclerà sull'array delle img dei loghi dei partner -->
        <template v-for="(partner, index) in partnersLogos">
            <li :key="index">
                <a :href="partner.link">
                    <img :src="partner.logo" alt="">
                </a>
            </li>
        </template>
    </ul>
</template>

<script>
export default {
    data() {
        return {
            partnersLogos: [
                {
                    logo: '../../assets/img/amazon.svg',
                    link: 'https://www.amazon.it/',
                },
                {
                    logo: '../../assets/img/google.svg',
                    link: 'https://www.google.it/',
                },
                {
                    logo: '../../assets/img/lenovo.svg',
                    link: 'https://www.lenovo.com/it/it/',
                },
                {
                    logo: '../../assets/img/paypal.svg',
                    link: 'https://www.paypal.com/it/home',
                }, 
                {
                    logo: '../../assets/img/shopify.svg',
                    link: 'https://it.shopify.com/',
                },
                {
                    logo: '../../assets/img/spotify.svg',
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
    li a {
        width: 80px;
        height: 30px;
    }
}

</style>