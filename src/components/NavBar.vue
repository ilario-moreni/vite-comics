<script>
    export default {
      name: 'NavBar',
      data(){
        return{
            sections: [
                {
                    label: 'CHARACTERS',
                    active: false,
                },

                {
                    label: 'COMICS',
                    active: false,
                },

                {
                    label: 'MOVIES',
                    active: false,
                    link: '#',
                },

                {
                    label: 'TV',
                    active: false,
                    link: '#',
                },

                {
                    label: 'GAMES',
                    active: false,
                    link: '#',
                },

                {
                    label: 'COLLECTIBLES',
                    active: false,
                    link: '#',
                },

                {
                    label: 'VIDEOS',
                    active: false,
                    link: '#',
                },

                {
                    label: 'FANS',
                    active: false,
                    link: '#',
                },

                {
                    label: 'NEWS',
                    active: false,
                    link: '#',
                },

                {
                    label: 'SHOP',
                    active: false,
                    link: '#',
                }
            ]
        }
      }  
    }
</script>

<template lang="">
    <div class="main_container">
        <div class="nav">
            <div>
                <img src="../assets/img/dc-logo.png"  class="DC_logo" alt="logo DC">
            </div>
            <ul class="section_ul">
                <li v-for='(section, index) in sections' :key="index">
                    <a class="section_a" :href="section.link">{{ section.label }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss">
    @use '../styles/partials/mixin.scss';

    .main_container{
        @include mixin.container;
    }

    .section_ul{
        @include mixin.ul_section;
    }

    .DC_logo{
        width: 100px;
    }

    .nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 140px;
    }
</style>