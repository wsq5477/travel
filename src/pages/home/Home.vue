<template>
   <div>
   	 <home-header></home-header>
   	 <home-swiper :swiperList="swiperList"></home-swiper>
   	 <home-icon :iconList="iconList"></home-icon>
   	 <home-recommend :detailList="detailList"></home-recommend>
   	 <home-weekend :weekList="weekList"></home-weekend>
   </div>
</template>
<script>
import homeHeader from './components/Header.vue'
import homeSwiper from './components/Swiper.vue'
import homeIcon from './components/Icon.vue'
import homeRecommend from './components/recommend.vue'
import homeWeekend from './components/Weekend.vue'
import axios from 'axios'

export default{
	name:"Home",
	components:{
		homeHeader,
		homeSwiper,
		homeIcon,
		homeRecommend,
		homeWeekend
	},
	data(){
		return{
			swiperList:[],
			iconList:[],
			detailList:[],
			weekList:[]
		}
	},
	methods:{
		getHomeInfo(){
			axios.get('/api/index.json')
			  .then(this.getHomeInfoSucc)
		},
		getHomeInfoSucc(res){
			res=res.data
			if(res.ret&&res.data)
			{
				const data=res.data
				this.swiperList=data.swiperList
				this.iconList=data.iconList
				this.detailList=data.detailList
				this.weekList=data.weekList
			}
		}
	},
	mounted(){
       this.getHomeInfo()
	}
}
</script>
<style>
</style>