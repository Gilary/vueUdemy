<template>
  <div class="container">  
    <Titel />
    <hr>
    <Server /> 
    <hr>
    <Footer />
  </div>
</template>

<script>
  import Titel from './Titel.vue';
  import Server from './Server.vue';
  import Footer from './Footer.vue';
  export default {
    components:{
      Titel,
      Server,
      Footer
    }
  }

</script>

<style>

</style>
