<!-- 
Componente diviso in tre parti
- 1: logo, descrizione e icone social
- 2: liste di links, che prendono ognuna la metà dello spazio
- 3: input per sottoscrizione alla newsletter 
-->

<template>
    <section id="foot-info" class="container flex-row">
        <!-- logo e social media icons -->
        <div id="social-box" class="col-4">
            <figure id="foot-logo"><img src="../../assets/img/logo-light.png"></figure>
            <p class="foot-paragraph">Start working with Landrick can provide everything you nedd to generate awareness, drive traffic, connect.</p>
            
            <span v-for="(icon, i) in socialList" :key="i" class="icon-wrapper"  > <!--  -->
                <a :href="icon.link"><font-awesome-icon :icon="icon.icon"  /></a>
            </span>
        </div>

        <!-- liste di link -->
        <div id="links-box" class="col-4 flex-row">
            <div class="col-2">
                <h3 class="foot-title">Company</h3>
                <ul>
                    <li v-for="(link, i) in companyLinks" :key="i" class="flex-row align-cx">
                        <font-awesome-icon icon="fa-solid fa-chevron-right" class="chevron-icon" /> <a href="#">{{ link }}</a>
                    </li>
                </ul>
            </div>

            <div class="col-2">
                <h3 class="foot-title">Usefull Links</h3>
                <ul>
                    <li v-for="(link, i) in usefullLinks" :key="i" class="flex-row align-cx">
                        <font-awesome-icon icon="fa-solid fa-chevron-right" class="chevron-icon" /> <a href="#">{{ link }}</a>
                    </li>
                </ul>
            </div>
        </div>

        <!-- newsletter -->
        <div id="newsletter-box" class="col-4">
            <h3 class="foot-title">Newsletter</h3>
            <p class="foot-paragraph">Sign up and receive the last tips via email.</p>
            <form action="">
                <label for="newsletter">Write your email <span class="redHeart">*</span></label> 
                <div id="input-wrapper">
                    <input type="text" placeholder="Your email"> 
                    <font-awesome-icon id="mail-icon" icon="fa-regular fa-envelope" />
                </div>
                <button>Subscribe</button>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            socialList: [
                {
                    social: 'Facebook',
                    link: 'https://www.facebook.com/',
                    icon: 'fa-brands fa-facebook-f',
                },
                {
                    social: 'Instagram',
                    link: 'https://www.instagram.com/',
                    icon: 'fa-brands fa-instagram',
                },
                {
                    social: 'Twitter',
                    link: 'https://twitter.com/?lang=it',
                    icon: 'fa-brands fa-twitter',
                },
                {
                    social: 'LinkedIn',
                    link: 'https://it.linkedin.com/',
                    icon: 'fa-brands fa-linkedin-in',
                },
            ],
            companyLinks: ['About us', 'Service', 'Team', 'Pricing', 'Project', 'Careers', 'Blog', 'Login'],
            usefullLinks: ['Terms of service', 'Privacy Policy', 'Documentation', 'Changelog', 'Components'],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/scss/colorPalette.scss';

#foot-info {
    gap: 10px;

    h3 {
        color: $footTitle;
    }

    .foot-paragraph {
        font-size: 0.9rem;
        margin: 20px 0;
    }

    #social-box {

        #foot-logo {
            max-width: 50%;
        }

        .icon-wrapper {
            border: 1px solid $footText;
            // font-size: 0.9rem;
            border-radius: 5px;
            margin-right: 7px;
            padding: 4px 9px;
            aspect-ratio: 1;
        }

        // --fa-border-color: $footText ;
        // --fa-border-padding: 7px;
        // --fa-border-radius: 5px;
        // --fa-pull-margin: 10px;
    }

    #links-box, #newsletter-box {
        padding: 5px;

        ul {
            padding: 15px 0;

            li {
                font-size: 0.8rem;
                // padding: 5px;
                line-height: 25px;
                // vertical-align: middle;
                gap: 10px;

                .chevron-icon {
                    font-size: 8px;
                    // vertical-align: middle; 
                    // padding-right: 5px;
                }
            }
        }
    }

    #newsletter-box {

        form {

            label {
                font-size: 0.8rem;
            }

            input, button {
                width: 100%;
                margin: 5px 0;
                // background-color: transparent;
            }

            #input-wrapper {
                position: relative;

                input {
                    background-color: $inputBkg;
                    padding: 10px;
                    border-radius: 7px;
                    padding-left: 40px;
                    border: none;
                    color: white;
                    // position: relative;
                }

                #mail-icon {
                    position: absolute;
                    left: 3%;
                    top: 50%;
                    transform: translateY(-50%);
                    font-size: 20px;   
                }
            }

            button {
                background-color: $btnBkg;
                border: none;
                color: $btnText;
                box-shadow: 0px 4px 5px -2px $btnsShadow;
            }
        }
    }
}
</style>