<script>
import dcComicsList from '../data/dc-comics.js';
import SerieCard from '../components/SerieCard.vue';
export default {
    name: 'Content',
    components: {
        dcComicsList,
        SerieCard,
    },
    data(){
        return{
          dcComics: dcComicsList  
        }
    }
}

</script>

<template lang="">
    <div class="content_div">
        <div class="jumbo_container">
        </div>
        <div class="currentseries_container">
            <div class="series_container">
                <div>
                    <h2 class="series_header">CURRENT SERIES</h2>
                </div>
                <div class="series_cards_container">
                    <SerieCard v-for="(item, index) in dcComics.dcComicsList"  :card="item" :key="index"/>
                </div>
            </div>
            <div class="load_more_button">
                <button>LOAD MORE</button>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    @use '../styles/partials/mixin.scss';
    @use '../styles/partials/variables.scss' as *;

    .content_div{
        @include mixin.container;
        width: 100%;
    }
    
    /* jumbo container */

    .jumbo_container{
        background-image: url('../assets/img/jumbotron.jpg');
        background-size: cover;
        height: 350px;
    }

    /* current-series container */

    .currentseries_container{
        background-color: #1C1C1C;
        padding-bottom: 2rem;
    }

    .series_container{
        @include mixin.container;
        position: relative;
        color:white;
    }

    .series_header{
        color:white;
        background-color: $lightblue;
        position: absolute;
        transform: translateY(-50%);
        padding: 1rem 2rem;
        font-size: 24px;
    }

    .series_cards_container{
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        row-gap: 3rem;
        padding: 3.5rem 1rem;
    }

    /* button */

    .load_more_button{
        display: inline-block;
        position:relative;
        left: 50%;
        button{
            transform:translateX(-50%);
            background-color: $lightblue;
            padding: 0.5rem 3rem;
            color: white;
            font-size: 14px;
            border:none;

            &:hover{
                filter: brightness(1.1);
                box-shadow: 0 1px 10px 1px black ;
            }
        }
    }

</style>