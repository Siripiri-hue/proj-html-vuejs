<!--
Componente diviso in due blocchi, divisi dallo space between:
- il primo contiene il "made with"
- il secondo contiene le icone dei metodi di pagamento possibili 
Più un terzo blocco, posizionato in absolute, per la freccia "torna su"
-->

<template>
    <section id="copyrights">
        <div class="container flex-row space-btw align-cx">
            <span id="made-by">&#169; Landrick. Designed with <span class="redHeart"><font-awesome-icon icon="fa-solid fa-heart" /></span> by Shreethemes.</span>

            <ul id="payment-methods" class="flex-row align-cx">
                <li v-for="(icon, i) in paymentIcons" :key="i">
                    <a :href="icon.link"><img :src="icon.src" alt=""></a>
                </li>
            </ul>
        </div>

        <div id="arrow-icon">
            <a href="#">
                <font-awesome-icon icon="fa-solid fa-arrow-up" />
            </a>
        </div>
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
@import '../../assets/scss/colorPalette.scss';

#copyrights {
    padding: 15px 0 10px;
    position: relative;
    border-top: 1px solid #232E4A;

    .container {
        padding: 10px 0;
    }
    
    ul {
        gap: 5px;

        li {
            max-width: 30px;
        }
    }

    #made-by {
        font-size: 0.8rem;
    }

    #arrow-icon {
        position: absolute;
        bottom: 35%;
        // transform: translateY(-50%);
        right: 20px;
        font-size: 0.8rem;
        // color: $btnText;
        background-color: $btnUpBkg;
        box-shadow: 0px 4px 5px -2px $btnsShadow;
        padding: 3px 7px;
        border-radius: 5px;
    }
}


</style>