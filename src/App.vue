<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12"></div>
			<kwot>
				<h2 slot="title">{{kwotTitel}}</h2>
				<p slot="content">kwot kwot</p>
			</kwot>
    </div>
  </div>
</template>

<script>
import Kwot from './components/Kwot.vue';
export default {
	data(){
		return {
			kwotTitel:'Kwoty'
		}
	},
  components: {
    Kwot
  }
};
</script>

<style>
	/* styling for slot NOT here but logics all up there/ now you can style here 2*/
</style>
