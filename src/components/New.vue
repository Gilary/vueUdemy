<template>
  <div>
    <h3>Nieuw</h3>
    <button @click="counter++">Meer!</button>
    <p>{{counter}}</p>
  </div>
</template>

<script>
export default {
  data(){
    return{
      counter:0
    };
  },
  destroyed(){
    console.log('kapot!')
  },
  deactivated(){
    console.log('gedeactiveerd!')
  },
  activated(){
    console.log('actief')
  }
};
</script>

<style scoped>
</style>
