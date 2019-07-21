<template>
    <div class="wrapper">
        <swiper :options="swiperOption" >
            <!-- slides -->
            <swiper-slide v-for="(item,index) in  swiperList" :key="item.id">
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
    },
    swiperList:[
        {
            id:"001",
            imgUrl:"https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/b72df47942fb28fcd7bf481f01e785f5.jpg"
        },
        {
            id:"002",
            imgUrl:"https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/0677c297245b8a489ee12ab9b165c928.jpg_945x288_600cb364.jpg"
        }, {
            id:"003",
            imgUrl:"https://h-des-activity-fecp.qunarzz.com/h_des_activity_fe_h_des_activity_fe/973dc1ae0da73a58410186df08ff25cb.jpg"
        }, {
            id:"004",
            imgUrl:"https://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/a685001bbf5e77a203ff8815e953efbe.jpg_945x288_52b6ec01.jpg"
        }
        ]

 }

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