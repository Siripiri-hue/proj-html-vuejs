<template>
    <section id="rates">
        <!-- componente diviso in due row:
        - la prima contiene il testo
        - la seconda le card, che verranno ciclate probabilmente da un altro componente -->
        <div class="title-wrapper-cx">
            <h2 class="section-title">Our rates from developer from Landrick team</h2>
            <p class="section-decription">Star working with <span class="brand">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
        </div>

        <div id="card-wrapper" class="flex-row">
            <div class="card" v-for="(subscript, index) in subscriptions" :key="index">
                <button class="label">{{ subscript.type }}</button>
                <h3 class="section-title">{{ subscript.price }}</h3>
                <p class="section-decription">{{ subscript.rate }}</p>
                <p class="section-decription">{{ subscript.description }}</p>
                <div class="section-decription flex-col">
                    <span v-for="(benefit, index) in subscript.benefits" :key="index">
                        <font-awesome-icon icon="fa-regular fa-circle-check" /> {{ benefit }}
                    </span>
                </div>
                <button class="blue-btn">Buy now</button>
                <p class="section-decription">* No credit card required</p>
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
#card-wrapper {
    gap: 15px;

    .card {
        // gap: 20px;
        padding: 15px;
        border: 1px solid grey;
        border-radius: 10px;
        box-shadow: 0px 3px 0px 0px #ADB5BD;

        .blue-btn {
            width: 100%;
        }
    }
}
</style>