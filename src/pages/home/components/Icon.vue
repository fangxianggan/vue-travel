<template>
    <div class="icons">
     <swiper >
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
      iconsList:[
          {
              id:"001",
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
              desc:"景点门票"
          },
           {
              id:"002",
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png",
              desc:"水上乐园"
          },
           {
              id:"003",
              imgUrl:"http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/3ef092d0a89ffddb7f781cda30c8ae49.png",
              desc:"暑期促销"
          },
           {
              id:"004",
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/f5/c4c9d9830404e602.png",
              desc:"室内娱乐"
          },
           {
              id:"005",
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png",
              desc:"动植物园"
          },
           {
              id:"006",
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png",
              desc:"世纪公园"
          },
           {
              id:"007",
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png",
              desc:"上海野生"
          },
           {
              id:"008",
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/de/f26be47a6bf02a02.png",
              desc:"上海迪士尼"
          },
           {
              id:"009",
              imgUrl:"https://img1.qunarzz.com/piao/fusion/1810/50/26ffa31b56646402.png",
              desc:"上海海昌"
          },{
              id:"010",
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/3e/86314b2af03b7502.png",
              desc:"清凉避暑"
          }
      ]

    }
       
  },
  computed:{
    pages (){
      const pages=[]
       this.iconsList.forEach((item,index)=>{
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