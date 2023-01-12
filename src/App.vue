<script>
 import NavBar from './components/NavBar.vue';
 import Content from './components/Content.vue';
 import Footer from './components/Footer.vue'
  export default {
    components: {
      NavBar,
      Content,
      Footer
    }
  }
</script>

<template lang="">
  <div>
    <NavBar />
    <Content />
    <Footer />
  </div>
</template>
<style lang="scss">
   @use './styles/generals.scss' as *;
</style>