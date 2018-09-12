<template>
  <div class="city-header">
  	<div class="city-select">城市选择</div>
  	<router-link to="/">
  	<div class="headerBack">
	<span class="iconfont iconLeft">&#xe628;</span>
     </div>
    </router-link>
  </div>
</template>
<script>
export default{
	name:"cityHeader"
}
</script>
<style lang="stylus">
   .city-header{
   	position:relavite;
   	background:#00bcd4;
   	height:.86rem;
   	line-height:.86rem;
   	color:#fff;
   	.city-select{
   		text-align:center;
   	    font-size:.3rem;
   	}
   	.headerBack{
   		  position:absolute;
   		  top:0;
   		  color:#fff;
          width:.6rem;
          text-align:center;
          .iconLeft{
          	padding-left:.2rem;
          	font-size:.4rem;
          }
    }
   }
   
</style>