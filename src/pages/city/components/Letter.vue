<template>
  <div class="letterList">
     <div class="letter">A</div>
     <div class="letter">A</div>
     <div class="letter">A</div>
     <div class="letter">A</div>
     <div class="letter">A</div>
     <div class="letter">A</div>
  </div>
</template>
<script>
export default{
	name:"cityLetter",
  
}
</script>
<style lang="stylus">
  .letterList{
    display:flex;
    flex-direction:column;
    justify-content:center;
    position:absolute;
    right:0;
    height:100%;
    width:.4rem;
    .letter{
      line-height:.4rem;
      color:#00bcd4;
      text-align:center;
    }
  }
</style>