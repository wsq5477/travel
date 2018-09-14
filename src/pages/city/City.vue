<template>
	<div>
		<city-header></city-header>
		<city-search :cities="cities"></city-search>
		<city-list :cities="cities" :hotCities="hotCities" :letter="letter"></city-list>
		<city-letter :cities="cities" @change="handleLetterChange"></city-letter>
	</div>
</template>
<script>
import axios from 'axios'
import cityHeader from './components/Header.vue'
import citySearch from './components/Search.vue'
import cityList from './components/List.vue'
import cityLetter from './components/Letter.vue'

export default{
	name:"City",
	components:{
		cityHeader,
		citySearch,
		cityList,
		cityLetter
	},
	data(){
       return{
       	   hotCities:[],
       	   cities:{},
       	   letter:""
       }
	},
	methods:{
		getCityInfo(){
			axios.get('/api/city.json')
			  .then(this.getCityInfoSucc)
		},
		getCityInfoSucc(res)
		{
			res=res.data
			if(res.ret&&res.data)
			{
				const data=res.data
				this.hotCities=data.hotCities
				this.cities=data.cities
			}
		},
		handleLetterChange(letter){
            this.letter=letter
		}
	},
	mounted(){
		this.getCityInfo()
	}
}
</script>
<style lang="stylus">
</style>