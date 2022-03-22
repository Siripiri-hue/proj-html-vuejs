<template>
    <section id="jumbo" class="flex-row align-cx">
        <!-- qui andrà il jumbo, diviso in due colonne:
        una conterrà il testo e i tasti, l'altra l'immagine -->

        <div class="col-2">
            <button class="label">Development</button>
            <h1 id="jumbo-title">A Complete Developer Toolset</h1>
            <p>Launch your campain and benefit from our expertise on designing and managing conversion centered bootstrap4 html page.</p>
            <div id="jumbo-btn">
                <button class="blue-btn">Get Started</button>
                <button class="white-btn">Documentation</button>
            </div>
            <p>Current Version: v2.6.0</p>
        </div>

        <div class="col-2">
            <img src="../../assets/img/about.png" alt="">
        </div>
    </section>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
#jumbo {
    padding: 25px;

    .col-2:first-child {
        #jumbo-title {
            line-height: 60px;
            width: 70%;
            font-size: 35px;
            font-weight: 700;
        }

        p {
            margin: 30px 0;
            line-height: 20px;
            color: #8f949b;
        }

        #jumbo-btn {
            margin: 30px 0;

            button:last-child {
                margin-left: 8px;
            }
        }
    }

    
}

</style>