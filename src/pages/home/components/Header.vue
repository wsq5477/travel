<template>
	<div class="header">
	  <div class="headerBack">
	  	<span class="iconfont iconLeft">&#xe628;</span>
	  </div>
	  <div class="headerContent">
        <span class="iconfont">&#xe648;</span>
	  	输入城市/景点/游玩主题
	  </div>
    <router-link to="/city">
	  <div class="headerCity">
	     {{this.city}}
	  <span class="iconfont traingle">&#xe662;</span>
	  </div>
  </router-link>
	</div>
</template>
<script>
import {mapState} from 'vuex'
export default{
	name:"HomeHeader",  
  computed:{
    ...mapState(['city'])   
  }
}
</script>
<style lang="stylus" scoped>
    .header{
         line-height:0.86rem;
         height:0.86rem;
         display:flex;  
         background:#00bcd4; 
         color:#fff;  
    }
    .headerBack{
    	  float:left;
          width:.6rem;
          text-align:center;
          .iconLeft{
          	padding-left:.2rem;
          	font-size:.4rem;
          }
    }
    .headerContent{
    	background:#fff;
    	color:#ccc;
    	margin-top:.12rem;
    	margin-left:.2rem;
    	height:.64rem;
    	line-height:.64rem;
    	flex:1;
    	border-radius:.1rem;
    	padding-left:.2rem;
    }
    .headerCity{
       float:right;
       min-width:1.08rem;
       padding:0 0.1rem; 
       text-align:center;
       color:#fff;
       .traingle{
       	  font-size:.2rem;
       }
    }
</style>