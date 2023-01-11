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
            ]
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
        <div class="main_container"></div>
        <div class="main_container"></div>
    </div>
</template>

<style lang="scss">
    @use './styles/partials/mixin.scss';
    @use './styles/partials/variables.scss' as *;

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
        color: white;
        justify-content: space-between;
    }

    .shop_icon{
        height: 70px;
        width: 70px;
        object-fit: contain;
        margin-right: 10px;
    }

    .shop_li_label{
        display: flex;
        align-items: center;
    }

</style>