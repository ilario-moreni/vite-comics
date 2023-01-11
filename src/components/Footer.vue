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
            }
        }
    }
}
</script>

<template lang="">
    <div>
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
        <div class="features_container">
            <div class="main_container features_lists_container">
                <div>
                    <ul class="features_ul">
                        <li>
                            <h3>DC COMICS</h3>
                        </li>
                        <li class="features_li" v-for="item in features.dc_Comics_list">
                            {{ item.label }}
                        </li>
                    </ul>
                    <ul class="features_ul">
                        <li>
                            <h3>SHOP</h3>
                        </li>
                        <li class="features_li" v-for="item in features.shop_list">
                            {{ item.label }}
                        </li>
                    </ul>
                </div>
                <div>
                    <ul class="features_ul">
                        <li>
                            <h3>DC</h3>
                        </li>
                        <li class="features_li" v-for="item in features.dc_list">
                            {{ item.label }}
                        </li>
                    </ul>
                </div>
                <div>
                    <ul class="features_ul">
                        <li>
                            <h3>SITES</h3>
                        </li>
                        <li class="features_li" v-for="item in features.sites_list">
                            {{ item.label }}
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="main_container"></div>
    </div>
</template>

<style lang="scss">

    @use './styles/partials/mixin.scss';
    @use './styles/partials/variables.scss' as *;

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
        min-height: 200px;
        max-height: 482px;
    }

    .features_lists_container{
        display: flex;
        margin: 0 auto;
        padding: 2rem 0;
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
        color: grey;
        font-size: 14px;
        line-height: 1.5rem;
    }

</style>