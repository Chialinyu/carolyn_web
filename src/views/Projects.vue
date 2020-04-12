<template>
	<div class="project">
		<h1>Projects</h1>

		<div class="components">

			<div class="component" v-for="project in projectList" v-bind:key="project.id" >
				<ProjectCell :project="project"/>
			</div>

		</div>

	</div>
</template>


<style lang="scss">
	.project{
		width: 80%;
		margin: 0 auto;
		height: 100%;
    	overflow: auto;
		
		.component{
			width: 40%;
			display: inline-block;
			padding: 15px 8px;
			// background: url("../assets/cell_bg.png");
			// background-color: #c89664;
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
  data:function(){
    return {
			projectList: [
				{id: 1, title: 'EyeBus', imgsrc: require('../assets/EyeBus.jpg'), teamMember: 'a and 3 others', date: 'July, 2020', description: 'Empowering Visually Impaired Passengers to Travel Independently by Bus'},
				{id: 2, title: 'WalkingVibe', imgsrc: require('../assets/walkingvibe.png'), teamMember: 'b and 3 others', date: 'April, 2020', description: 'Reducing Virtual Reality Sickness in VR using Vibrotactile Feedback'},
				{id: 3, title: 'WoTrust', imgsrc: require('../assets/woTrust.jpg'), teamMember: 'c and 2 others', date: 'July, 2020', description: 'A Patient-safety Reporting Tool for Doctors'},
				{id: 4, title: 'DLIOR Descriptor', imgsrc: require('../assets/dlior.png'), teamMember: 'a and 4 others', date: 'Aug, 2019', description: 'Descriptor based on Local Intensity Order Relations of Pixel Group'},
				{id: 5, title: 'Medi-self', imgsrc: require('../assets/MediSelf.jpg'), teamMember: 'a and 3 others', date: 'Oct, 2018', description: 'A Tool to Improve Drug Adherence'},
				{id: 6, title: 'ReMind', imgsrc: require('../assets/Remind.jpg'), teamMember: 'a and 3 others', date: 'Aug, 2017', description: 'Arouse the deep emotions'},
				{id: 7, title: 'EoE! Empathy of Earth', imgsrc: require('../assets/eoe.jpg'), teamMember: 'a and 3 others', date: 'April, 2017', description: 'Interactive Storytelling Light'},
			]
    }; 
	},

});
</script>