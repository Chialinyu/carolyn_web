<template>
  <div id="app">
    		<div id="nav" :style="{'height': navHeight + 'px'}">
			<div class="title">
				CAROLYN YU
			</div>
			<div class="buttoms">
				<div class="buttom"><router-link to="/">Home</router-link></div> |
				<div class="buttom"><router-link to="/projects">Project</router-link></div> |
				<div class="buttom"><a href="#">CV</a></div>
			</div>
		</div>
    <div class="router-content" :style="{'height': height}">
      <router-view/>
    </div>
  </div>
</template>

<style lang="scss">
* {
  box-sizing: border-box;
}

@font-face {
  font-family: desdemon;
  src: url(./assets/desdemon.ttf);
}

body,
html {
  padding: 0;
  margin: 0;
  // height: 100%;
  /*		background: rgba( 100, 100, 100, 0.1);*/
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #868686;
}

#nav {
  margin-top: 30px;
  // height: 100%;
  // padding: 30px 0 0 0;
  // height: 100px;
  /*		background: rgba(255, 255, 255, 0.2);*/

  a {
    font-weight: bold;
    color: #868686;
    &.router-link-exact-active {
      color: #ff8686;
    }
  }

  .title {
    /*			padding: 30px;*/
    font-size: 40px;
    width: 20%;
    margin: auto;
    font-family: desdemon;
    border-bottom: 0.5px solid rgba(0, 0, 0, 0.2);
  }

  .buttom {
    display: inline-block;
    padding: 15px 5%;
  }
}

  .router-content{
    overflow: hidden;
  }

</style>

<script lang="ts">
import Vue from "vue";
//import ProjectCell from '@/components/ProjectCell.vue'; // @ is an alias to /src

export default Vue.extend({
  name: "app",

  data:function(){
    return{
      navHeight: 100, 
      height: "auto",
    }
  },

  created: function(){
    window.addEventListener("resize", this.getHeight);
  },

  mounted: function(){
    this.getHeight();
    console.log("hi");
  },

  methods: {
    getHeight :function() {
      let navDOM: any = document.getElementById("nav");
      let navHeight = navDOM.getBoundingClientRect().bottom;
      let windowHeight = window.innerHeight;
      console.log(navDOM.getBoundingClientRect(), navHeight, window.innerHeight);
      this.height = windowHeight - navHeight + "px";
    }

  },

});
</script>

