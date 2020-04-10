<template>
	<div class="cell">
		<div class="coverimg">
			<!-- <img src="../assets/bg.png"> -->
			<img src="../assets/EyeBus.jpg">
		</div>
		<h3> Project Name </h3>
		<p>
			Team member / MM, YYYY <br>
			short description about this project.
		</p>

	</div>
</template>

<style scoped lang="scss">
	
	.cell{
		padding: 6px;
		border-width: 0.5px; 
		border-color: rgba(0, 0, 0, 0.2); 
		border-style: solid;
	}
	
	img{
		width: 100%;
		// height: 100%;
		opacity: 0.5;
		// background-color: #c89664;
	}
	
	h3 {
		margin: 40px 0 0;
	}
	ul {
		list-style-type: none;
		padding: 0;
	}
	li {
		display: inline-block;
		margin: 0 10px;
	}
	a {
		color: #ff8686;
	}
</style>


<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'PrjectCell',
  props: {
    //msg: String,
  },
});
</script>
