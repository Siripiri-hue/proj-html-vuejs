<!-- 
Questo componente contiene due blocchi, così divisi:
- il primo contiene una col centrata, il quale a suo volta contiene il titolo e il sottotitolo della section
- il secondo contiene il riquadro dei comandi npm ecc 
-->

<template>
    <section>
        <div class="col-2">
            <h6 class="brand">Quickstart</h6>
            <h2 class="section-title">Awesome, isn't it? Let's dive in!</h2>
            <p class="section-description">Start working with <span class="brand">Landrick</span> that can provide everything you have to generate awareness, drive traffic, connect.</p>
        </div>

        <div>
            <div id="commands-line">
                <div id="btn-wrapper" class="flex-row just-cx">
                    <button class="btn-command" v-for="(btn, index) in commandLines" :key="index"
                    :class="{ active: index === activeBtn }"
                    @click="changeActiveElem(index)">
                        {{ btn }}
                    </button>
                </div>
                <p><span class="greenColor">$</span> npm install <span class="greenColor">-g</span> claps.js</p>
            </div>
            <div id="benefits">
                <span><font-awesome-icon icon="fa-regular fa-circle-check" class="greenColor"/> Organize you own data</span>
                <span><font-awesome-icon icon="fa-regular fa-circle-check" class="greenColor"/> Work with any team</span>
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
    },

    methods: {
        changeActiveElem: function(index) {
            this.activeBtn = index;
        }
    } 
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/colorPalette.scss';

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
        background-color: $commandBkg;
        border-radius: 5px;
        padding: 15px;

        #btn-wrapper {
            // padding: 25px;
            // padding: 10px 0;
            border: 1px solid $btnBorder;
            border-radius: 5px;
            background-color: $btnBorder;

            .btn-command {
                flex-grow: 1;
                border: none;
                color: white;
                background-color: transparent;

                &.active {
                    background-color: $activeBkg;
                }
            }
        }

        p {
            margin: 20px 0 10px 2px;
        }
    }

    #benefits {
        color: $benefitsText;
        // max-width: fit-content;
        
        span {
            padding-right: 25px;
            line-height: 50px;
        }
    }
} 

</style>