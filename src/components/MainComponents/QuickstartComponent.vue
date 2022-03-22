<template>
    <section>
        <!-- questo componente contiene due row, così divise:
        - la prima contiene una col centrata che contiene il titolo e il sottotitolo della section
        - la seconda contiene il riquadro dei comandi npm ecc -->

        <div class="col-2">
            <h6 class="brand">Quickstart</h6>
            <h2>Awesome, isn't it? Let's dive in!</h2>
            <p class="section-decription">Start working with <span class="brand">Landrick</span> that can provide everything you have to generate awareness, drive traffic, connect.</p>
        </div>

        <div>
            <div id="commands-line">
                <div id="btn-wrapper" class="flex-row just-cx">
                    <button class="btn-command" v-for="(btn, index) in commandLines" :key="index"
                    :class="{ active: index === activeBtn }">
                        {{ btn }}
                    </button>
                </div>
                <p>$ npm install -g claps.js</p>
            </div>
            <div id="benefits">
                <span><font-awesome-icon icon="fa-regular fa-circle-check" /> Organize you own data</span>
                <span><font-awesome-icon icon="fa-regular fa-circle-check" /> Work with any team</span>
            </div>
        </div>

    </section>
</template>

<script>
export default {
    data() {
        return {
            commandLines: ['npm', 'nuget', 'spm', 'github'],
            activeBtn: 0,
        }
    }    
}
</script>

<style lang="scss" scoped>
.col-2 {
    margin: 0 auto;
    text-align: center;
}

div:last-of-type {
    margin: 0 auto;
    // max-width: fit-content;
    // padding: 20px;
    color: white;
    max-width: 600px;

    #commands-line {
        // height: 125px;
        background-color: #3C4858;
        border-radius: 5px;
        padding: 15px;

        #btn-wrapper {
            // padding: 25px;
            // padding: 10px 0;
            border: 1px solid #576271;
            border-radius: 5px;
            background-color: #4F5A69;

            .btn-command {
                flex-grow: 1;
                border: none;
                color: white;
                background-color: transparent;

                &.active {
                    background-color: #3C4858;
                }
            }
        }

        p {
            margin: 20px 0 10px 2px;
        }
    }

    #benefits {
        color: #8D9AAC;
        // max-width: fit-content;
        
        span {
            padding-right: 25px;
            line-height: 50px;
        }
    }
} 

</style>