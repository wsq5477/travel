<template>
	<div class="icons">
	   <div class="icon" v-for="item of iconList" :key="item.id">
	   	 <div class="icon-img">
	 	   <img class="icon-img-content" :src="item.imgUrl">
	 	 </div>
	 	  <p class="icon-text">{{item.text}}</p>
	   </div>
    </div>
</template>
<script>
export default{
	name:"HomeIcon",
	data(){
		return{
			iconList:[{
				id:"001",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
				text:"景点门票"
			},
			{
				id:"002",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png",
				text:"夏日玩水"
			},
			{
				id:"003",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
				text:"一日游"
			},
			{
				id:"004",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png",
				text:"自然风光"
			},
			{
				id:"005",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png",
				text:"全部玩乐"
			}]
		}
	}
}
</script>
<style lang="stylus">
.icons{
	margin-top:.15rem;
	display:flex;
	flex-wrap:wrap;
   overflow:hidden;
   padding-bottom:50.67%;
   height:0;
   .icon{
   	  position:relative;
   	  overflow:hidden;
   	  width:25%;
   	  height:0;
   	  padding-bottom:20%;
   	  .icon-img{
   	  	position:absolute;
   	  	top:0;
   	  	right:0;
   	  	left:0;
   	  	bottom:.44rem;
   	  	.icon-img-content{
   	  		height:100%;
   	  		display:block;
   	  		margin:0 auto;
   	  	}
   	  }
   	  .icon-text{
   	  	position:absolute;
   	  	right:0;
   	  	left:0;
   	  	bottom:0;
   	  	height:.44rem;
   	  	line-height:.44rem;
   	  	text-align:center;
   	  }
   }
}
</style>