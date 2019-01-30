<template>
  <div class="col-xs-12 col-sm-6">
    <ul class="list-group">
      <Server v-for="server in servers" :server="server" />
    </ul>
  </div>
</template>

<script>
import Server from './Server.vue';

export default {
  data (){
		return{
			servers: [
				{ id: 1, status: 'Normaal'},
				{ id: 2, status: 'Kritiek'},
				{ id: 3, status: 'Onbekend'},
				{ id: 4, status: 'Raar'}
			]
		};
	},
	//props:['servers'],
	components:{
		Server
	}
};
</script>

<style>
</style>
