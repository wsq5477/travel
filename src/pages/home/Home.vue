<template>
   <div>
   	 <home-header></home-header>
   	 <home-swiper></home-swiper>
   	 <home-icon></home-icon>
   	 <home-recommend></home-recommend>
   </div>
</template>
<script>
import homeHeader from './components/Header.vue'
import homeSwiper from './components/Swiper.vue'
import homeIcon from './components/Icon.vue'
import homeRecommend from './components/recommend.vue'

export default{
	name:"Home",
	components:{
		homeHeader,
		homeSwiper,
		homeIcon,
		homeRecommend,
	}
}
</script>
<style>
</style>