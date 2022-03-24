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
                <div class="card-description flex-col">
                    <span v-for="(benefit, index) in subscript.benefits" :key="index">
                        <font-awesome-icon icon="fa-regular fa-circle-check" /> {{ benefit }}
                    </span>
                </div>
                <button class="blue-btn">Buy now</button>
                <p class="card-description">* No credit card required</p>
                <div id="best-rate" v-show="(index ===1)">Best</div>
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

#card-wrapper {
    gap: 15px;

    .card {
        // gap: 20px;
        padding: 15px;
        border: 1px solid $cardBorder;
        border-radius: 10px;
        box-shadow: 0px 3px 0px 0px $cardRateShadow;
        position: relative;
        color: $sectionText;
        font-weight: 700;

        .title-wrapper {
            margin: 15px 0;
        }

        .card-title {
            color: black;
            font-size: 1.7rem;
        }

        .card-subtitle {
            font-size: 0.8rem;
        }
        
        .card-details {
            font-size: 0.8rem;

            &::after {
                content: "";
                display: block;
                border-bottom: 1px solid $darkCardBorder;
                width: 100%;
                margin: 15px 0;
            }
        }

        .blue-btn {
            width: 100%;
        }

        #best-rate {
            position: absolute;
            top: 10px;
            right: 5px;
            background-color: $bandBkg;
            transform: rotate(40deg);
            color: white;
            font-size: 0.6rem;
            padding: 3px;
        }

        &:hover {
            transform: scale(1.05);
            box-shadow: 0px 3px 0px 0px $blueBtn, 17px 2px 20px -4px rgba(159,159,159,0.5), -17px 2px 20px -4px rgba(159,159,159,0.5);
            // box-shadow: 17px 2px 20px 0px rgba(159,159,159,0.5);
            // box-shadow: -17px 2px 20px 0px rgba(159,159,159,0.5);
        }
    }
}
</style>