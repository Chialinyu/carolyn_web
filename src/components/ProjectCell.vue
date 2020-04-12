<template>
	<div class="cell" >
		<div class="coverimg">
			<!-- <img src="../assets/bg.png"> -->
			<img :src="project.imgsrc">
		</div>
		<h3> {{project.title}} </h3>
		<p>
			<!-- {{project.teamMember}} 
			/ -->
			{{project.date}}
		</p>
		<p>
			{{project.description}}
		</p>

	</div>

</template>

<style scoped lang="scss">
	
	.cell{
		padding: 6px;
		border-width: 0.5px; 
		border-color: rgba(0, 0, 0, 0.2); 
		border-style: solid;

		opacity: 0.5;
		transition: .3s ease;
	}
	
	.cell:hover {
		opacity: 1;
		box-shadow: 0px 2px 18px 0px rgba(0,0,0,0.75);
	}

	img{
		width: 100%;
		// height: 100%;
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
		color: #c89664;
	}
</style>


<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'PrjectCell',
  props: ['project'],

});
</script>
