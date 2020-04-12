<template>
	<!-- <div class="home" :style="{ 'max-height': `calc(100vh - ${getNavHeight}px)`}"> -->
  <div class="home">

		<div class="avatar">
			<img alt="profile" src="../assets/me.png" style="border-radius: 50%">
			<p> &#10077; Carolyn Yu</p>
			<p> &#10000; 游佳霖 </p>
			<p> RA in Innovative User Interface Lab at NTUST.</p>
			<br>
			<p> &#9992; Taipei, Taiwan</p>
			<p> &#9993; Email </p>


		</div>

		<div class="info">
			<h1>About</h1>
			Hi, I'm Carolyn, research assistant in <a href="http://nccuiuilab.github.io/index.html" target="_blank"> Innovation User Interface Lab </a> at National Taiwan University of Science and Technology lead by <a href="#" target="_blank">Prof. Neng-Hao Yu</a>.

			<br>.<br>.<br>.
			<p> QAQ </p>
			<br>

			<h1>Publications</h1>

      <h4> WalkingVibe: Reducing Virtual Reality Sickness and Improving Realism while Walking in VR using Unobtrusive Head-mounted Vibrotactile Feedback </h4>
			Yi-Hao Peng, <b>Carolyn Yu</b>, Shi-Hong Liu, Chung-Wei Wang, Paul Taele, Neng-Hao Yu, and Mike Y. Chen
			<p>CHI 2020 <a href="https://www.yihaopeng.tw/pdf/CHI20_WalkingVibe_preprint.pdf"> [PDF] </a> </p>

      <h4> BusMyFriend: Designing a Bus Reservation Service for People with Visual Impairments in Taipei City </h4>
			<b>Carolyn Yu</b>, Yee Li, Tsai-Yuan Huang, Wei-An Hsieh, Shao-Yu Lee, I-Hui Yeh, Gang Ku Lin, Neng-Hao Yu, Hsien-Hui Tang, and Yung-Ju Chang
			<p>DIS Pwip 2020 <a href="#"> [PDF] </a> </p>

			<h4> Construction and Optimization of Feature Descriptor based on Dynamic Local Intensity Order Relations of Pixel Group</h4>
			Wen-Hung Liao, <b>Carolyn Yu</b>, and Yi-Chieh Wu
			<p>ICIAR 2019 <a href="https://doi.org/10.1007/978-3-030-27202-9_33"> [PDF] </a> </p>

			<h1>Education</h1>
			<p> M.S., Computer Science 2017</p>
			<p> Visual Information Processing Lab</p>
			<p> National Chengchi University</p>
			<br>
			<p> B.S., Computer Science 2015 </p>
			<p> Double major, Digital Content &amp; Technologies Program </p>
			<p> National Chengchi University</p>

			<br><br><br>
		</div>

	</div>

</template>

<style lang="scss">
.home {
  display: flex;
  overflow: hidden;
  height: 100%;
  padding: 20px;

  .avatar {
    flex: 1;
    text-align: left;
    padding: 40px;
    border-right: 0.5px solid rgba(0, 0, 0, 0.5);
    height: 100%;
    overflow: auto;

    img {
      width: 200px;
    }
  }
  .info {
    flex: 3;
    text-align: left;
    padding: 40px;
    height: 100%;
    overflow: auto;

    a {
      // color: #ff8686;
      color: #c89664;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }
    a:visited {
      text-decoration: none;
    }
    a:any-link {
      cursor: auto;
    }
  }
}
</style>

<script lang="ts">
import Vue from "vue";
//import ProjectCell from '@/components/ProjectCell.vue'; // @ is an alias to /src

export default Vue.extend({
  name: "home",
  components: {
    //ProjectCell
  },
  computed: {
    getNavHeight() {
      // const navDOM = document.getElementById("nav");
      // // console.log(navDOM.getBoundingClientRect().bottom);
      // return navDOM ? navDOM.getBoundingClientRect().bottom : 0;
    }
  }
});
</script>
