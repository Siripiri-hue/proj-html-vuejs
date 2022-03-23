<!--
Questo componente contiene la nav, la quale contiene tre blocchi, allineati con il flex e sono:
- il logo
- la lista dei link della navbar
- la lista delle icone in alto a dx 
-->

<template>
    <nav>
        <!-- immagine del logo -->
        <figure id="logo">
            <img src="../../assets/img/logo-dark.png">
        </figure>

        <!-- lista di links presenti nella navbar -->
        <!-- anziché fare un altro componente, ciclo direttamente sul codice -->
        <ul id="nav-links">
            <li v-for="(item, index) in navList" :key="index"
            :class="{ active: index === activeLink }" 
            @click="changeActiveLink(index)">
            <!-- :class="(index === activeLink) ? 'active' : ''">  -->
                <a href="#">
                    {{ item }}
                    <font-awesome-icon icon="fa-solid fa-chevron-down" v-show="(item != 'Home')" />
                </a>
            </li>
        </ul>

        <!-- icone in alto a dx -->
        <div id="nav-icons">
            <a href="#">
                <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
            </a>

            <!-- anziché fare un altro componente, ciclo direttamente sul codice -->
            <button v-for="(item, index) in icons" :key="index"> 
                <a :href="item.link">
                    <font-awesome-icon :icon="item.icon" />
                </a>
            </button>

            <!-- <button>
                <a href="https://github.com/">
                    <font-awesome-icon icon="fa-brands fa-github" />
                </a>
            </button>
            <button>
                <a href="https://stackoverflow.com/">
                    <font-awesome-icon icon="fa-brands fa-stack-overflow" />
                </a>
            </button>
            <button>
                <a href="#">
                    <font-awesome-icon icon="fa-regular fa-user" />
                </a>
            </button> -->
        </div>
    </nav>
</template>

<script>
export default {
    data() {
        return {
            navList: [
                "Home",
                "Landing",
                "Pages",
                "Docs"
            ],

            activeLink: 0,

            icons: [
                {
                    link: 'https://github.com/',
                    icon: 'fa-brands fa-github',
                },
                {
                    link: 'https://stackoverflow.com/',
                    icon: 'fa-brands fa-stack-overflow',
                },
                {
                    link: '#',
                    icon: 'fa-regular fa-user',
                }
            ]
        }
    },

    methods: {
        changeActiveLink: function(index) {
            this.activeLink = index;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/colorPalette.scss';

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: $darkGrey;

    #logo {
        width: 130px;
    }

    #nav-links {
        display: flex;
        gap: 20px;
        text-transform: uppercase;
        font-size: 10px;
        font-weight: 700;

        .active {
            color: $LandrickViolet;
        }
    }

    #nav-icons {
        display: flex;
        gap: 7px;
        align-items: center;
        // font-size: 10px;
    
        button {
            background-color: $labelBkg;
            color: $blueBtn;
            padding: 5px 7px;
            border: none;
            border-radius: 5px;
            box-shadow: 4px 4px 5px -1px rgba(106,106,106,0.88);
        }
    }
}

</style>