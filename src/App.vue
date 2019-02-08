<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12"></div>
			<button @click="selectedComponent = 'Kwot'">Kwot</button>
			<button @click="selectedComponent = 'Author'">Autur</button>
			<button @click="selectedComponent = 'New'">Nieuw</button>
			<hr>
			<keep-alive>
				<component :is="selectedComponent">Waarde</component>
			</keep-alive>
			<!-- <kwot>
				<h2 slot="title">{{kwotTitel}}</h2>
				<p>kwot kwot</p>
			</kwot> -->
    </div>
  </div>
</template>

<script>
import Kwot from './components/Kwot.vue';
import Author from './components/Author.vue';
import New from './components/New.vue';
export default {
	data(){
		return {
			kwotTitel:'Kwoty',
			selectedComponent: 'Kwot'
		}
	},
  components: {
		Kwot,
		Author,
		New

  }
};
</script>

<style>
	/* styling for slot NOT here but logics all up there/ now you can style here 2*/
</style>
