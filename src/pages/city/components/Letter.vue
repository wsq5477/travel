<template>
  <div  class="letterList">
    <div v-for="(item,key) of cities" :key="key">
     <div class="letter">{{key}}</div>
   </div>
  </div>
</template>
<script>
export default{
  props:{
    cities:Object
  },
  name:"cityLetter",
  
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