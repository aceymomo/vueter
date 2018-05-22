<template>
  <div>
    <home-header></home-header>
    <home-swiper :swiper-msg="swipermsg"></home-swiper>
    <home-icons :icon-msg="iconsMsg"></home-icons>
    <home-recommend :recommend-msg="recommendMsg"></home-recommend>
    <home-weekend :weekend-msg="weekendMsg"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from '@/pages/home/components/header'
import HomeSwiper from '@/pages/home/components/Swiper'
import HomeIcons from '@/pages/home/components/Icons'
import HomeRecommend from '@/pages/home/components/Recommend'
import HomeWeekend from '@/pages/home/components/Weekend'
import axios from 'axios'
import {mapState} from 'vuex'
export default {
  name:'Home',
  data(){
    return {
      lastCity:'',
      swipermsg:[],
      iconsMsg:[],
      recommendMsg:[],
      weekendMsg:[]
    }
  },
  computed:{
    ...mapState(['city'])
  },
  components:{
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  methods:{
    getHomeInfo(){
      axios.get('/api/index.json?city=' + this.city)
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc(res){
      res = res.data
      if(res.ret && res.data){
        const data = res.data
        this.swipermsg = data.swiperList
        this.iconsMsg = data.iconList
        this.recommendMsg = data.recommendList
        this.weekendMsg = data.weekendList
        console.log(this.recommendMsg)
      }
    }
  },
  mounted(){
    this.lastCity = this.city
    this.getHomeInfo()
  },
  activated(){
    if(this.lastCity !== this.city){
      this.lastCity = this.city
      this.getHomeInfo()
    }
  }
}
</script>

<style>

</style>


