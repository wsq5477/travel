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
	data(){
		return{
			detailList:[{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_140x140_73fda71d.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1702/df/df60e318301fd2a2a3.water.jpg_200x200_e900c10e.jpg',
        title: '韶山游客换乘中心',
        desc: '韶山游客换乘，韶山的必经之路'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201301/16/afede9aa94dda9c193835fbb.jpg_200x200_c87b7e36.jpg',
        title: '韶山旅游区',
        desc: '毛泽东故乡，充满文人色彩的旅游胜地'
      }]
		}
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