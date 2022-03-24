<!-- 
Questa sezione contiene due blocchi: il primo l'ingranaggio, posizionato in absoluto rispetto alla section;
il secondo, il jumbo vero e proprio, diviso in due colonne che prendono ognuna metà dello spazio:
una conterrà il testo e i buttons, l'altra l'immagine 
-->

<template>
    <section id="jumbo">
        <!-- icona ingranaggio -->
        <div id="gear-icon">
            <a href="#">
                <font-awesome-icon icon="fa-solid fa-gear" />
            </a>
        </div>
        
        <!-- blocco che contiene la colonna con il testo e l'img -->
        <div id="jumbo-wrapper" class="container flex-row align-cx">
            <!-- colonna con testo e buttons -->
            <div class="col-2">
                <button class="label">Development</button>
                <h1 id="jumbo-title">A Complete Developer Toolset</h1>
                <p class="section-description">Launch your campain and benefit from our expertise on designing and managing conversion centered bootstrap4 html page.</p>
                <div id="jumbo-btn">
                    <button class="blue-btn">Get Started</button>
                    <button class="white-btn">Documentation</button>
                </div>
                <p class="section-description">Current Version: v2.6.0</p>
            </div>

            <!-- colonna con l'img -->
            <div class="col-2">
                <img src="../../assets/img/about.png" alt="">
            </div>
        </div>
    </section>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/colorPalette.scss';

#jumbo {
    // padding: 25px;
    position: relative;

    #gear-icon {
        position: absolute;
        top: 5%;
        left: 0;
        background-color: white;
        border-bottom-right-radius: 20px;
        border-top-right-radius: 20px;
        color: $blueBtn;
        padding: 7px;
    }

    .col-2:first-child {
        #jumbo-title {
            line-height: 60px;
            width: 70%;
            font-size: 35px;
            font-weight: 700;
        }

        p {
            // margin: 30px 0;
            line-height: 20px;
            font-size: 1rem;
        }

        #jumbo-btn {
            margin: 30px 0;

            button:last-child {
                margin-left: 8px;
            }
        }
    }
    
    .col-2:last-child {
        padding: 50px;
    }
}

</style>