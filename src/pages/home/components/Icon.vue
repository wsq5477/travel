<template>
	<div class="icons">
	   <div class="icon" v-for="item of iconList" :key="item.id">
	 	  <img class="icon-img-content" :src="item.imgUrl">
	 	  <p class="icon-text">{{item.text}}</p>
	   </div>
    </div>
</template>
<script>
export default{
	name:"HomeIcon",
    props:{
    	iconList:Array
    }
}
</script>
<style lang="stylus">
.icons{
	margin-top:.15rem;
	display:flex;
	flex-wrap:wrap;
   overflow:hidden;
   height:3.5rem;
   .icon{
   	  width:25%;
   	  height:1.75rem;
   	  .icon-img-content{
   	  	width:1.2rem;
   	  	height:1.2rem;
   	  	display:block;
   	  	margin:0 auto;
   	  }
   	  .icon-text{
   	  	line-height:.14rem;
   	  	height:.14rem;
   	  	text-align:center;
   	  }
   }
}
</style>