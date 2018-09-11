<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="detail-list" v-for="item of weekList" :key="item.id">
        <img :src="item.imgUrl" class="detail-img">
        <div class="detail-text">
          <p class="detail-title">{{item.title}}</p>
          <p class="detail-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default{
  name:"HomeRecommend",
  props:{
    weekList:Array
  }
}
</script>
<style lang="stylus" scoped>
.title{
  width:100%;
  height:.8rem;
  line-height:.8rem;
  background:#eee;
    text-indent:.4rem;
}
.detail-list{ 
  .detail-img{
       width:100%;
  }
  .detail-text{
       padding:.1rem;
       .detail-title{
         line-height:.50rem;
         font-size:.32rem;
         white-space:nowrap;
          overflow: hidden;
          text-overflow: ellipsis;
       }
       .detail-desc{
          line-height: .4rem;
          color: #ccc;
          white-space:nowrap;
          overflow:hidden;
          text-overflow:ellipsis;
       }
  }
}
</style>