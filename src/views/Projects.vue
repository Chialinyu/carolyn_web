<template>
	<div class="project">
		<h1>Projects</h1>

		<div class="components">
			<div class="component" v-for="project in [1, 2, 3, 4, 5, 6]"  v-bind:key="project"> 
        <ProjectCell/> 
			</div>
		</div>

	</div>
</template>


<style lang="scss">
	.project{
		width: 80%;
		margin: 0 auto;
		height: calc(100vh - 100px);
/*		overflow: hidden;*/

/*
		.components{
			overflow: auto;
		}
*/
		
		.component{
			width: 40%;
			display: inline-block;
			padding: 6px;
			background: url("../assets/cell_bg.png");
			background-size: cover;
		}
	}

</style>

<script lang="ts">
import Vue from 'vue';
import ProjectCell from '@/components/ProjectCell.vue'; // @ is an alias to /src

export default Vue.extend({
  name: 'projects',
  components: {
    ProjectCell,
  },
  data:{
    length: [1, 2, 3, 4, 5, 6],
  },
});
</script>