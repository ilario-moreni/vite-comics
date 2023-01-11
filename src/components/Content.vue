<script>

export default {
    name: 'Content'
}
</script>

<template lang="">
    <div class="content_div">
        <h1>
        'Content Goes Here '
        </h1>
    </div>
</template>

<style lang="scss">
    @use './styles/partials/mixin.scss';
    .content_div{
        @include mixin.container;
        background-color: black;
        color:white;
        height: 150px;
        width: 100%;
    }
</style>