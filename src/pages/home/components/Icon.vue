<template>
    <div class="icons">
     <swiper :options="swiperOption">
      <swiper-slide v-for="(page,i) of pages">
      <div class="icon" v-for="(item,index) of page" :key="index">
       <div class="icon-img" >
         <img class="icon-img-content" 
         :src="item.imgUrl" 
         :alt="item.desc" style="opacity: 1;">
         <p class="icon-desc">{{item.desc}}</p>
       </div>
       </div>
        </swiper-slide>
       </swiper>
    </div>
</template>
<script>
 export default{
  name:"Icon",
  data (){
    return {
      swiperOption:{}
    }
  },
  props:{
    list:Array
  },
  computed:{
    pages (){
      const pages=[]
       this.list.forEach((item,index)=>{
          const page=Math.floor(index/8)
          if(!pages[page])
          {
           pages[page]=[]
          }
          pages[page].push(item)
       })
       return pages
    }
  }
 }
</script>


<style lang="stylus" scoped>
@import "~styles/varibles.styl"
@import "~styles/mixins.styl"
 .icons >>> .swiper-container
  overflow: hidden
  height: 0
  padding-bottom: 50%
  .icon
   position: relative
   overflow: hidden
   height: 0
   float: left
   width: 25%
   padding-bottom: 25%
   .icon-img
    position: absolute
    top: 0
    left: 0
    right: 0
    bottom: .44rem
    box-sizing: border-box
    padding: .1rem
    .icon-img-content
     height: 100%
     display: block
     margin: 0 auto
   .icon-desc
    position: absolute
    left: 0
    right: 0
    height: .44rem
    line-height: .44rem
    color: $darkTextColor
    ellipsis()
</style>