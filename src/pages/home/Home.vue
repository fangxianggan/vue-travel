<template>
 <div>
 <header-app></header-app>
 <home-swiper></home-swiper>
 <home-icon></home-icon>
 </div>
</template>


<script>
import Header from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcon from './components/Icon'
export default {
  name:'Home',
  components:{
    "header-app":Header,
    HomeSwiper,
    HomeIcon
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
