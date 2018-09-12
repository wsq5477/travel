<template>
	<div>
		<city-header></city-header>
		<city-search></city-search>
		<city-list></city-list>
		<city-letter></city-letter>
	</div>
</template>
<script>
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
	}
}
</script>
<style lang="stylus">
</style>