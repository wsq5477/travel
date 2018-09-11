<template>
   <div>
   	 <home-header></home-header>
   	 <home-swiper></home-swiper>
   	 <home-icon></home-icon>
   	 <home-recommend></home-recommend>
   	 <home-weekend></home-weekend>
   </div>
</template>
<script>
import homeHeader from './components/Header.vue'
import homeSwiper from './components/Swiper.vue'
import homeIcon from './components/Icon.vue'
import homeRecommend from './components/recommend.vue'
import homeWeekend from './components/Weekend.vue'

export default{
	name:"Home",
	components:{
		homeHeader,
		homeSwiper,
		homeIcon,
		homeRecommend,
		homeWeekend
	}
}
</script>
<style>
</style>