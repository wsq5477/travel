<template>
  <div class="city-search">
  	  <input v-model="keyword" type="text" name="城市搜索" placeholder="输入城市名或名称" class="search-input">
      <div class="searchList" ref="search" v-show="keyword">
        <div>
        <div class="searchItem border-bottom"  v-for="item of list" :key="item.id"  @click="handleNowCity(item.name)">{{item.name}}</div>
        <div class="searchItem border-bottom" v-show="hasNoData">没有找到匹配数据</div>
        </div>
      </div>
  </div>
</template>
<script>
import Bscroll from 'better-scroll'
export default{
	name:"citySearch",
  props:{
    cities:Object
  },
  data(){
    return{
      keyword:"",
      timer:null,
      list:[]
    }
  },
  computed:{
      hasNoData()
      {
        return !this.list.length
      }
  },
  mounted(){
     this.scroll=new Bscroll(this.$refs.search)
  },
  watch:{
    keyword(){
       if(this.timer)
       {
          clearTimeout(this.timer)
       }
       if(!this.keyword)
       {
          this.list=[];
          return
       }
       this.timer=setTimeout(()=>{
           const result=[]
           for(let i in this.cities){
            this.cities[i].forEach((value)=>{
               if(value.spell.indexOf(this.keyword)>-1||value.name.indexOf(this.keyword)>-1)
               {
                  result.push(value)
               }
            })
           }
           this.list=result
       },100)
    }
  },
  methods:{
    handleNowCity(city)
    {
       this.$store.commit('changeCity',city)
       this.$router.push('/')
    }
  }
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
      .searchList{
        position:absolute;
        top:1.57rem;
        right:0;
        left:0;
        bottom:0;
        overflow:hidden;
        z-index:1;
        background:#eee;
        .searchItem{
          line-height:.62rem;
          background:#fff;
          color:#666;
          text-indent:.2rem;
        }
      }
   }
</style>