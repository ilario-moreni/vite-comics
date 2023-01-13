<script>
    export default {
        name: 'SerieCard',
        props: {
            card: Object,
        }
    }
</script>
<template lang="">
    <div class="card">
        <img class="card_image" :src="card.thumb" :alt="card.series">
        <p class="series_name">{{ card.series }}</p>
    </div>
</template>
<style lang="scss">


    .card{
        width: calc(100% / 6);
    }

    .card_image{
        width: 190px;
        height: 190px;
        object-fit: cover;
        object-position: top;
        margin-bottom: 1rem;
    }

    .series_name{
        text-transform: uppercase;
        width: 190px;
    }
</style>