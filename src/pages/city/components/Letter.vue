<template>
  <div  class="letterList">
    <div v-for="item of letters" :key="item" :ref="item" @click="handleLetter" @touchstart="handleTouchStart" @touchend="handleTouchEnd" @touchmove="handleTouchMove">
     <div class="letter">{{item}}</div>
   </div>
  </div>
</template>
<script>
export default{
  props:{
    cities:Object,
  },
  data(){
    return{
          touchStatus:false
    }
  },
  computed:{
     letters(){
      const letters=[]
         for(let i in this.cities)
         { 
            letters.push(i)
         }
         return letters;
     }
  },
  name:"cityLetter",
  methods:{
     handleLetter(e){
        this.$emit("change",e.target.innerText)
     },
     handleTouchStart(){
         this.touchStatus=true
     },
     handleTouchMove(e){
        if(this.touchStatus)
        {
            const startY=this.$refs['A'][0].offsetTop
            const touchY=e.touches[0].clientY-79
            const index=Math.floor((touchY-startY)/20)
            if(index>=0&&index<=this.letters.length)
              this.$emit("change",this.letters[index])
        }
     },
     handleTouchEnd(){
        this.touchStatus=false
     }
  }
  
}
</script>
<style lang="stylus">
  .letterList{
    display:flex;
    flex-direction:column;
    justify-content:center;
    position:absolute;
    top:1.57rem;
    right:0;
    bottom:0;
    width:.4rem;
    .letter{
      line-height:.4rem;
      color:#00bcd4;
      text-align:center;
    }
  }
</style>