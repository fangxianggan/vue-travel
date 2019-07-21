<template>
 <div>
 <header-app></header-app>
 <home-swiper></home-swiper>
 23232
 </div>
</template>


<script>
import Header from './components/Header'
import HomeSwiper from './components/Swiper'
export default {
  name:'Home',
  components:{
    "header-app":Header,
    HomeSwiper
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
