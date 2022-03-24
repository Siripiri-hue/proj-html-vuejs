<template>
    <section class="col-2">
        <!-- componente che contiene due row:
        la prima avrà il testo e la seconda l'input -->

        <h2 class="section-title">Want to be among the first to find out?</h2>
        <p class="section-description">Start with <span class="brand">Landrick</span> that can provide everything you need to generate awareness, drive traffic, connect.</p>
        <form action="">
            <input type="text" placeholder="Email Address">
            <button class="blue-btn">Get Started</button>
        </form>
    </section>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/colorPalette.scss';

.col-2 {
    margin: 0 auto;
    text-align: center;

    form {
        position: relative;

        input {
            line-height: 35px;
            width: 100%;
            // position: relative;
            border: 1px solid lightgray;
            border-radius: 25px;
            padding: 0 20px;
        }

        button {
            position: absolute;
            right: 3px;
            top: 50%;
            transform: translateY(-50%);
            border-radius: 25px;
            box-shadow: 0px 4px 5px -2px $btnsShadow;
        }
    }
}
</style>