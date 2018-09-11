<template>
  <div class="swiper">
	<swiper :options="swiperOption" v-if="showSwiper">
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
	props:{
		swiperList:Array
	},
	data () {
		return{
			swiperOption:{
                loop:true,
                autoplay:3000,
                pagination:'.swiper-pagination'
			}
		}
	},
	computed:{
		showSwiper(){
			return this.swiperList.length
		}
	}
}
</script>
<style lang="stylus">
.swiper{
   overflow:hidden;
   width:100%;
   height:0;
   padding-bottom:26.7%;
   .swiper-pagination-bullet-active{
   	 background:#eee;
   }
  .swiper-img{
  	width:100%;
  }
}
</style>