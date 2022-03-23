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
                <h3 class="section-title">{{ subscript.price }}</h3>
                <p class="section-description">{{ subscript.rate }}</p>
                <p class="section-description">{{ subscript.description }}</p>
                <div class="section-description flex-col">
                    <span v-for="(benefit, index) in subscript.benefits" :key="index">
                        <font-awesome-icon icon="fa-regular fa-circle-check" /> {{ benefit }}
                    </span>
                </div>
                <button class="blue-btn">Buy now</button>
                <p class="section-description">* No credit card required</p>
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

        .blue-btn {
            width: 100%;
        }
    }
}
</style>