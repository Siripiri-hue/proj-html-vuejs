<!-- 
Il componente è diviso in due blocchi:
- il primo contiene il testo
- il secondo le card, ciclate
-->

<template>
    <section id="rates">
        <div class="title-wrapper-cx">
            <h2 class="section-title">Our rates from developer from Landrick team</h2>
            <p class="section-description">Star working with <span class="brand">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
        </div>

        <div id="card-wrapper" class="flex-row">
            <div class="card" v-for="(subscript, index) in subscriptions" :key="index">
                <button class="label">{{ subscript.type }}</button>
                <div class="title-wrapper">
                    <h3 class="card-title">{{ subscript.price }}</h3>
                    <p class="card-subtitle">{{ subscript.rate }}</p>
                </div>
                <p class="card-details">{{ subscript.description }}</p>
                <div class="card-benefits flex-col">
                    <span v-for="(benefit, index) in subscript.benefits" :key="index">
                        <span class="blue-text"><font-awesome-icon icon="fa-regular fa-circle-check" /></span> {{ benefit }}
                    </span>
                </div>
                <button class="blue-btn">Buy now</button>
                <p class="card-notes">* No credit card required</p>
                <div class="best-rate best-rate-top-right" v-show="(index === 1)">
                    <span>Best</span>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            subscriptions: [
                {
                    type: 'Basic',
                    price: '$9.00',
                    rate: 'Per Month',
                    description: 'All the basics for business that are you just getting started.',
                    benefits: [
                        'Full Access', 'Enhanced Security', 'Source Files', '1 Domain Free', 'Enhanced Security'
                    ]
                },
                {
                    type: 'Business',
                    price: '$39.00',
                    rate: 'Per Month',
                    description: 'All the basics for business that are you just getting started.',
                    benefits: [
                        'Full Access', 'Enhanced Security', 'Source Files', '1 Domain Free', 'Enhanced Security'
                    ]
                },
                {
                    type: 'Enterprise',
                    price: '$79.00',
                    rate: 'Per Month',
                    description: 'All the basics for business that are you just getting started.',
                    benefits: [
                        'Full Access', 'Enhanced Security', 'Source Files', '1 Domain Free', 'Enhanced Security'
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/colorPalette.scss';
@import '../../assets/scss/bestRateBand.scss';

.title-wrapper-cx {
    margin: 0 auto 60px;
    max-width: 60%;
    text-align: center;
}

#rates {
    margin-bottom: 80px;
}

#card-wrapper {
    gap: 15px;
    margin-bottom: 20px;

    .card {
        // gap: 20px;
        padding: 15px;
        border: 1px solid $cardBorder;
        border-radius: 10px;
        box-shadow: 0px 3px 0px 0px $cardRateShadow;
        position: relative;
        color: $sectionText;
        font-weight: 700;
        // overflow: hidden;
        font-size: 0.9rem;

        .title-wrapper {
            margin: 15px 0;
        }

        .card-title {
            color: black;
            font-size: 1.7rem;
        }

        // .card-subtitle, .card-details, .card-notes {
        //     font-size: 0.8rem;
        // }
        
        .card-details::after {
            content: "";
            display: block;
            border-bottom: 1px solid $darkCardBorder;
            width: 100%;
            margin: 15px 0;
        }

        .card-benefits {
            margin: 20px 0;

            span{
                margin: 5px 0;

                .blue-text {
                    margin-right: 5px;
                }
            }
        }

        .blue-btn {
            width: 100%;
            margin-bottom: 10px;
        }

        .card-notes {
            font-size: 0.8rem;
        }

        // #best-rate {
        //     position: absolute;
        //     top: 10px;
        //     right: -45px;
        //     background-color: $bandBkg;
        //     transform: rotate(40deg);
        //     color: white;
        //     font-size: 0.6rem;
        //     padding: 3px 60px;
        // }

        &:hover {
            transform: scale(1.05);
            box-shadow: 0px 3px 0px 0px $blueBtn, 17px 2px 20px -4px rgba(159,159,159,0.5), -17px 2px 20px -4px rgba(159,159,159,0.5);
            // box-shadow: 17px 2px 20px 0px rgba(159,159,159,0.5);
            // box-shadow: -17px 2px 20px 0px rgba(159,159,159,0.5);
        }

        &::before {
            content: "*";
            display: block;
            position:absolute;
            top: 10px;
            right: -45px;
        }

        // &::after {
        //     content: "ciao";
        // }
    }
}
</style>