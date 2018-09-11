<template>
  <div class="swiper">
	<swiper :options="swiperOption">
    <!-- slides -->
       <swiper-slide v-for="item of swiperList" :key="item.id">
       	  <img class="swiper-img" :src="item.imgUrl" alt="去哪儿门票">
       </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
 </div>
</template>
<script>
export default{
	name:"HomeSwiper",
	data () {
		return{
			swiperOption:{
                loop:true,
                autoplay:3000,
                pagination:'.swiper-pagination'
			},
			swiperList:[{
				id:"001",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1706/b8/a8e8ff02b094c802.jpg_750x200_ddaec8e5.jpg"
			},
			{
				id:"002",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1809/2d/0d7dc3400a50b502.jpg_750x200_4ca95dd4.jpg"
			},
			{
				id:"003",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1807/66/e5a5cec881702f02.jpg_750x200_67bb5691.jpg"
			},
			{
				id:"004",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1808/8a/1957a0fb58ad0402.jpg_750x200_e72b8c0f.jpg"
			},
			{
				id:"005",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1809/ce/bca92895556c5002.jpg_750x200_cf56d46c.jpg"
			},
			{
				id:"006",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/eb/f3d2fa5308fd5f02.jpg_750x200_38b8d6f7.jpg"
			},
			{
				id:"007",
				imgUrl:"http://img1.qunarzz.com/piao/fusion/1706/b9/6b91b49794f46402.jpg_750x200_d7f254e2.jpg"
			}]
		}
	}
}
</script>
<style lang="stylus">
.swiper{
   overflow:hidden;
   width:100%;
   height:0;
   padding-bottom:37.5%;
   .swiper-pagination-bullet-active{
   	 background:#eee;
   }
  .swiper-img{
  	width:100%;
  }
}
</style>