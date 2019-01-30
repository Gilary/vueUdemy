<template>
  <div class="col-xs-12 col-sm-6">
    <p v-if="!server">AUB selecteer server</p>
		<p v-else>Server #{{ server.id }} selected, Status:{{ server.status}}</p>
		<hr>
    <button @click="resetServer">reset server</button>
  </div>
</template>

<script>
//import Servers from "./Servers";
import { serverBus } from '../../main.js'

export default {
	data(){
		return{
			server: null
		}
	},
	methods: {
		resetServer() {
			this.server.status = 'Normaal';
		}
	},
	created() {
		serverBus.$on('serverSelected', (server) =>{
			this.server = server;
		})
	}
}
</script>

<style>
</style>
