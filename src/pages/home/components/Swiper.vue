<template>
    <div class="wrapper">
        <swiper :options="swiperOption" >
            <!-- slides -->
            <swiper-slide v-for="(item,index) in  list" :key="item.id">
            <img :src="item.imgUrl" class="swiper-img">
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>  
        </swiper>
    </div>
 
</template>

<script>
export default{
name:"SWiper",
data() {
 return {
    swiperOption:{
      pagination: '.swiper-pagination',
      loop:true
    }
 }
},
props:{
  list:Array
}
}
</script>

<style lang="stylus" scope>
 .wrapper >>> .swiper-pagination-bullet-active
    background: red !important
 .wrapper
    width: 100%
    height: 0
    overflow: hidden
    padding-bottom: 31.25%
    backgroud:#eee
    .swiper-img
     width: 100%
</style>