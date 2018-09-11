<template>
	<div>
		<div class="title">热销推荐</div>
		<ul>
			<li class="detail-list" v-for="item of detailList" :key="item.id">
				<img :src="item.imgUrl" class="detail-img">
				<div class="detail-text">
					<p class="detail-title">{{item.title}}</p>
					<p class="detail-desc">{{item.desc}}</p>
					<button class="btn">查看详情</button>
				</div>
			</li>
		</ul>
	</div>
</template>
<script>
export default{
	name:"HomeRecommend",
	props:{
    detailList:Array
  }
}
</script>
<style lang="stylus" scoped>
.title{
	width:100%;
	height:.8rem;
	line-height:.8rem;
	background:#eee;
    text-indent:.4rem;
}
.detail-list{
	display:flex;
	overflow: hidden;
	height:1.6rem;
	margin:.1rem 0 .1rem .1rem;
	padding-bottom:.1rem;
	.detail-img{
       width:1.6rem;
       height:1.6rem;
	}
	.detail-text{
		flex:1;
       padding:.1rem;
       .detail-title{
       	 line-height:.50rem;
       	 font-size:.32rem;
         white-space:nowrap;
          overflow: hidden;
          text-overflow: ellipsis;
       }
       .detail-desc{
          line-height: .4rem;
          color: #ccc;
          white-space:nowrap;
          overflow:hidden;
          text-overflow:ellipsis;
       }
       .btn{
       	  line-height: .44rem;
       	  background: #ff9300;
          color:#fff;
          border-radius:.06rem;
          padding:0 .2rem;
          margin-top:.16rem;
       }
	}
}
</style>