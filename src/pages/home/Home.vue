<template>
   <div>
   	 <home-header></home-header>
   	 <home-swiper></home-swiper>
   	 <home-icon></home-icon>
   </div>
</template>
<script>
import homeHeader from './components/Header.vue'
import homeSwiper from './components/Swiper.vue'
import homeIcon from './components/Icon.vue'

export default{
	name:"Home",
	components:{
		homeHeader,
		homeSwiper,
		homeIcon,
	}
}
</script>
<style>
</style>