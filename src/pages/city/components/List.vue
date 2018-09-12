<template>
  <div class="cityList" ref="wrapper">
    <div>
    <div class="area">
  	  <div class="title">当前城市</div>
      <div class="btnWrapper">
       <div class="btnList">
         <div class="btn">北京</div>
       </div>
     </div>
    </div>
    <div class="area">
      <div class="title">热门城市</div>
      <div class="btnWrapper">
       <div class="btnList">
         <div class="btn">北京</div>
       </div>
       <div class="btnList">
         <div class="btn">北京</div>
       </div>
       <div class="btnList">
         <div class="btn">北京</div>
       </div>
       <div class="btnList">
         <div class="btn">北京</div>
       </div>
       <div class="btnList">
         <div class="btn">北京</div>
       </div>
       <div class="btnList">
         <div class="btn">北京</div>
       </div>
       <div class="btnList">
         <div class="btn">北京</div>
       </div>
     </div>
    </div>
    <div class="area">
      <div class="title">A</div>
      <div class="itemList">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title">A</div>
      <div class="itemList">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title">A</div>
      <div class="itemList">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
    <div class="area">
      <div class="title">A</div>
      <div class="itemList">
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
        <div class="item border-bottom">阿拉尔</div>
      </div>
    </div>
  </div>
  </div>
</template>
<script>
import Bscroll from 'better-scroll'
export default{
	name:"cityList",
  mounted(){
     this.scroll=new Bscroll(this.$refs.wrapper)
  }
}
</script>
<style lang="stylus">
.border-bottom{
  &:before{
    border-color:#ccc;
  }
}
.cityList{
  overflow:hidden;
  position:absolute;
  top:1.57rem;
  left:0;
  right:0;
  bottom:0;
  .area{
   .title{
      line-height:.44rem;
      background:#eee;
      text-indent:.1rem;
      font-size:.26rem;
      color:#666;
   }
   .btnWrapper{
    display:flex;
    flex-wrap:wrap;
    padding-right:.6rem;
     .btnList{
      width:33.33%;
      .btn{
        margin:.1rem;
        border:.01rem solid #ccc;
        text-align:center;
        border-radius:.06rem;
        padding:.1rem;
      }
     }
   }
   .itemList{
     .item{
       line-height:.70rem;
       text-indent:.2rem;
     }
   }
}
}
</style>