<template>
<div class="header">
<div class="header-left">
<span class="iconfont">&#xe624;</span>
</div> 
<div class="header-input">
<span class="iconfont">&#xe632;</span>
输入城市/景点/游玩主题
</div>
<div class="header-right">
{{city}}
<span class="iconfont"  >&#xe62d;</span>
</div>
</div>

</template>

<script>
export default {
  name: 'Header',
  props:{
    city:String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
@import "~styles/varibles.styl"
.header
  display: flex
  line-height: .86rem
  background: $bgColor
  color: #fff
  .header-left
    width: .64rem
    float: left
  .header-input
    flex: 1
    background: #fff
    border-radius: .1rem
    margin-top: .12rem
    height: .64rem
    line-height: .64rem
    margin-left: .2rem
    color: #ccc
  .header-right
    width: 1.24rem
    float: right
    text-algin: center

</style>
