<template>
   <div>
   	 <home-header></home-header>
   	 <home-swiper></home-swiper>
   </div>
</template>
<script>
import homeHeader from './components/Header.vue'
import homeSwiper from './components/Swiper.vue'

export default{
	name:"Home",
	components:{
		homeHeader,
		homeSwiper
	}
}
</script>
<style>
</style>