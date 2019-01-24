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
  import Titel from './components/Shared/Titel.vue';
  import Server from './components/Server/Server.vue';
  import Footer from './components/Shared/Footer.vue';
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
