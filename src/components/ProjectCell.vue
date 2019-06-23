<template>
	<div class="cell">
		<div>
			<img src="../assets/bg.png">
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
	}
	
	img{
		width: 100%;
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
