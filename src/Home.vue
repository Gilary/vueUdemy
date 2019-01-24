<template>
  <div>
    <p>server status: {{ status }}</p>
    <hr>
    <button @click="changeStatus">verander status</button>
  </div>
</template>

<script>
export default {
  data(){
    return{
        status: 'critical'
    }
  },
  methods: {
    changeStatus() {
      this.status = 'Normal';
    }

  }
}
</script>

<style>

</style>


