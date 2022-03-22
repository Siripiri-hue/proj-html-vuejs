<template>
    <nav>
        <!-- questo componente contiene una row (la nav), che contiene tre blocchi, i quali sono allineati con il flex e sono:
        - il logo
        - la lista dei link della navbar
        - la lista delle icone in alto a dx -->

        <!-- immagine del logo -->
        <figure id="logo">
            <img src="../../assets/img/logo-dark.png">
        </figure>

        <!-- lista di links presenti nella navbar -->
        <ul id="nav-links">
            <template v-for="(item, index) in navList" > <!-- anziché fare un altro componente, dal momento che non verrà riutilizzato, ciclo una porzione di codice -->
                <li :key="index"> 
                    <a href="">{{ item }}</a>
                </li>
            </template>
        </ul>

        <!-- icone in alto a dx -->
        <div id="nav-icons">
            <a href="#">
                <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
            </a>

            <template v-for="(item, index) in icons" > <!-- anziché fare un altro componente, dal momento che non verrà riutilizzato, ciclo una porzione di codice -->
                <button :key="index"> 
                    <a :href="item.link">
                        <font-awesome-icon :icon="item.icon" />
                    </a>
                </button>
            </template>

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
    }
}
</script>

<style lang="scss" scoped>
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #44505F;

    #logo {
        width: 130px;
    }

    #nav-links {
        display: flex;
        gap: 20px;
        text-transform: uppercase;
        font-size: 10px;
        font-weight: 700;
    }

    #nav-icons {
        display: flex;
        gap: 7px;
        align-items: center;
        // font-size: 10px;
    
        button {
            background-color: #E4E9F8;
            color: #2F55D4;
            padding: 5px 7px;
            border: none;
            border-radius: 5px;
            box-shadow: 4px 4px 5px -1px rgba(106,106,106,0.88);
        }
    }


}

</style>