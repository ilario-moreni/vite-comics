<script>
export default {
    name: 'Footer',
    data(){
        return{
            products: [
                {
                    name:'DIGITAL COMICS',
                    url:'buy-comics-digital-comics.png'
                },

                {
                    name:'DC MERCHANDISE',
                    url:'buy-comics-merchandise.png'
                },

                {
                    name:'SUBSCRIPTION',
                    url:'buy-comics-subscriptions.png'
                },

                {
                    name:'COMIC SHOP LOCATOR',
                    url:'buy-comics-shop-locator.png'
                },

                {
                    name:'DC POWER VISA',
                    url:'buy-dc-power-visa.svg'
                }
            ],
            features: {
                dc_Comics_list: [
                    {
                        label:'Characters',
                        link: '#'
                    },
                    {
                        label:'Comics',
                        link: '#'
                    },
                    {
                        label:'Movies',
                        link: '#'
                    },
                    {
                        label:'TV',
                        link: '#'
                    },
                    {
                        label:'Games',
                        link: '#'
                    },
                    {
                        label:'Videos',
                        link: '#'
                    },
                    {
                        label:'News',
                        link: '#'
                    }
                ],
                shop_list: [
                    {
                        label:'Shop DC',
                        link: '#'
                    },
                    {
                        label:'Shop DC Collectibles',
                        link: '#'
                    }
                ],
                dc_list: [
                    {
                        label:'Terms Of Use',
                        link: '#'
                    },
                    {
                        label:'Privacy policy (New)',
                        link: '#'
                    },
                    {
                        label:'Ad Choices',
                        link: '#'
                    },
                    {
                        label:'Advertising',
                        link: '#'
                    },
                    {
                        label:'Jobs',
                        link: '#'
                    },
                    {
                        label:'Subscriptions',
                        link: '#'
                    },
                    {
                        label:'Talent Workshops',
                        link: '#'
                    },
                    {
                        label:'CPSC Certificates',
                        link: '#'
                    },
                    {
                        label:'Ratings',
                        link: '#'
                    },
                    {
                        label:'Shop Help',
                        link: '#'
                    },
                    {
                        label:'Contact Us',
                        link: '#'
                    }
                ],
                sites_list: [
                    {
                        label:'DC',
                        link: '#'
                    },
                    {
                        label:'MAD Magazine',
                        link: '#'
                    },
                    {
                        label:'DC Kids',
                        link: '#'
                    },
                    {
                        label:'DC Universe',
                        link: '#'
                    },
                    {
                        label:'DC Power Visa',
                        link: '#'
                    }
                ]
            },
            socials: [
                {
                    src:'footer-facebook.png',
                    link:'#',
                },
                {
                    src:'footer-twitter.png',
                    link:'#',
                },
                {
                    src:'footer-youtube.png',
                    link:'#',
                },
                {
                    src:'footer-pinterest.png',
                    link:'#',
                },
                {
                    src:'footer-periscope.png',
                    link:'#',
                }
            ]
        }
    }
}
</script>

<template lang="">
    <div>
        <!-- top footer container -->
        <div class="top_footer_container">
            <div class="main_container">
                <ul class="shop_ul">
                    <li v-for="(item, index) in products" :key="index" class="shop_li_label">
                        <img class="shop_icon" :src="`./src/assets/img/${item.url}`" alt="">
                        {{ item.name }}
                    </li>
                </ul>
            </div>
        </div>

        <!-- features container -->
        <div class="features_container">
            <div class="main_container features_lists_container">
                <div>
                    <ul class="features_ul">
                        <li>
                            <h3>DC COMICS</h3>
                        </li>
                        <li class="features_li" v-for="item in features.dc_Comics_list">
                            <a :href="item.link"> {{ item.label }} </a>
                        </li>
                    </ul>
                    <ul class="features_ul">
                        <li>
                            <h3>SHOP</h3>
                        </li>
                        <li class="features_li" v-for="item in features.shop_list">
                            <a :href="item.link"> {{ item.label }} </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <ul class="features_ul">
                        <li>
                            <h3>DC</h3>
                        </li>
                        <li class="features_li" v-for="item in features.dc_list">
                            <a :href="item.link"> {{ item.label }} </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <ul class="features_ul">
                        <li>
                            <h3>SITES</h3>
                        </li>
                        <li class="features_li" v-for="item in features.sites_list">
                            <a :href="item.link"> {{ item.label }} </a>
                        </li>
                    </ul>
                </div>
                <img class="dc_logo_bg" src="/src/assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
        <div class="socials_container">
            <div class="flex_container">
                <div>
                    <button class="sign_up_button">
                        SIGN-UP NOW!
                    </button>
                </div>
                <div class="right_socials_container">
                    <div class="follow_us">FOLLOW US</div>
                    <div>
                        <img v-for="item in socials" class="social_icons" :src="`/src/assets/img/${item.src}`" alt="">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">

    @use '../styles/partials/mixin.scss';
    @use '../styles/partials/variables.scss' as *;

    /* top footer container */

    .top_footer_container{
        background-color: $lightblue;
        padding: 2rem;
    }

    .main_container{
        @include mixin.container;
    }

    .shop_ul{
        @include mixin.flat_ul;
        @include mixin.ul_style_none;
        @include mixin.my_li;
        color: white;
        justify-content: space-between;
    }

    .shop_icon{
        height: 60px;
        width: 60px;
        object-fit: contain;
        margin-right: 10px;
    }

    .shop_li_label{
        display: flex;
        align-items: center;
    }

    /* features container */

    .features_container{
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        position: relative;
        z-index: -2;
    }

    .features_lists_container{
        display: flex;
        position: relative;
        padding: 1.5rem 0;
        height: 100%;
        h3{
            color:white;
            margin: 1.5rem 0 1rem;
        }
    }

    .features_ul{
        @include mixin.ul_style_none;
        width: 180px;
    }

    .features_li{
        font-size: 12px;
        line-height: 1.5rem;
        a{
            color: $grey;
            z-index: 100;
        }
    }

    .dc_logo_bg{
        position: absolute;
        right: 5%;
        bottom: -20%;
        z-index: -1;
    }

    /* socials container */

    .socials_container{
        background-color: #303030;
        padding: 2.5rem 0;
    }

    .flex_container{
        @include mixin.flex_container;
    }

    .sign_up_button{
        border: 2px solid $lightblue;
        background-color: transparent;
        color:white;
        padding: 1rem;
    }

    .right_socials_container{
        display: flex;
        align-items: center;
    }

    .follow_us{
        color: $lightblue;
        cursor:pointer;
    }

    .social_icons{
        margin-left: 1rem;
        cursor:pointer;


        &:hover{
            filter: brightness(1.5);
        }
    }


</style>