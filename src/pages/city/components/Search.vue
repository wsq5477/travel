<template>
  <div class="city-search">
  	  <input type="text" name="城市搜索" placeholder="输入城市名或名称" class="search-input">
  </div>
</template>
<script>
export default{
	name:"citySearch"
}
</script>
<style lang="stylus">
   .city-search{
      background:#00bcd4;
      height:.72rem;
      padding:0 .1rem;
      .search-input{
        box-sizing:border-box;
         text-align:center;
         width:100%;
         height:.62rem;
         font-size:.1rem;
         color:#666;
         padding:0 .1rem;
         border-radius:.06rem;
      }
   }
</style>