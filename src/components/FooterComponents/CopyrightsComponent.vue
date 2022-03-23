<template>
    <section id="copyrights" class="flex-row space-btw align-cx">
        <!-- componente diviso in due colonne:
        - la prima che contiene il "made with"
        - la seconda contiene le icone dei metodi di pagamento possibili -->

        <span>&#169; Landrick. Designed with <font-awesome-icon icon="fa-solid fa-heart" /> by Shreethemes.</span>

        <ul id="payment-methods" class="flex-row align-cx">
            <li v-for="(icon, i) in paymentIcons" :key="i">
                <a :href="icon.link"><img :src="icon.src" alt=""></a>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    data() {
        return {
            paymentIcons: [
                {
                    name: 'amex',
                    src: require('../../assets/img/american-ex.png'),
                    link: 'https://www.americanexpress.com/it-it/',
                },
                {
                    name: 'discover',
                    src: require('../../assets/img/discover.png'),
                    link: 'https://www.discoverglobalnetwork.com/',
                },
                {
                    name: 'mastercard',
                    src: require('../../assets/img/master-card.png'),
                    link: 'https://www.mastercard.it/it-it.html',
                },
                {
                    name: 'paypal',
                    src: require('../../assets/img/paypal.png'),
                    link: 'https://www.paypal.com/it/home',
                },
                {
                    name: 'visa',
                    src: require('../../assets/img/visa.png'),
                    link: 'https://www.visaitalia.com/',
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
#copyrights {
    padding: 30px 0 10px;

    ul {
        gap: 5px;

        li {
            max-width: 40px;
        }
    }
}
</style>