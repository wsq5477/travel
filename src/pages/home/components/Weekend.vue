<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="detail-list" v-for="item of detailList" :key="item.id">
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
  data(){
    return{
      detailList:[{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/ae/11f076c6cb7c47.jpg_r_640x214_6f643489.jpg',
        title: '张家界必游TOP10',
        desc: '到张家界最值得游玩的地方'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fb/302620ed8350f8.jpg_r_640x214_25a07cb4.jpg',
        title: '长沙必游TOP10',
        desc: '到了长沙，一定要到这些地方走走'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/56/33894ef918e1a8.jpg_r_640x214_a9de6b4e.jpg',
        title: '湘西必游TOP10',
        desc: '神奇山水风水，浓郁民俗风情'
      }]
    }
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