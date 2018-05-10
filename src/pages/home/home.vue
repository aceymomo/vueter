<template>
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>
</template>

<script>
import HomeHeader from '@/pages/home/components/header'
import HomeSwiper from '@/pages/home/components/Swiper'
import HomeIcons from '@/pages/home/components/Icons'
export default {
  name:'Home',
  components:{
      HomeHeader,
      HomeSwiper,
      HomeIcons
    }
}
</script>

<style>

</style>


