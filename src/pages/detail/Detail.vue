<template>
  <div>
    <detail-banner
      :sightName="sightName"
      :bannerImg="bannerImg"
      :bannerImgs="gallaryImgs"
    ></detail-banner>
    <detail-header></detail-header>
    <div class="home">
      <detail-list :list="list"></detail-list>
    </div>
    
  </div>
</template>

<script type="text/ecmascript-6">
import DetailBanner from '@/pages/detail/components/banner'
import DetailHeader from '@/pages/detail/components/Header'
import DetailList from '@/pages/detail/components/List'
import axios from 'axios'
  export default {
    name:"Detail",
    data() {
      return {
        sightName:'',
        bannerImg:'',
        gallaryImgs:[],
        list:[],
      }

    },
    components: {
      DetailBanner,
      DetailHeader,
      DetailList
    },
    methods:{
      getDetailInfo(){
        axios.get('/api/detail.json',{
          params:{
            id:this.$route.params.id
          }
        })
          .then(this.handleGetDetailInfo)
      },
      handleGetDetailInfo(res){
        res = res.data
        if(res.ret && res.data){
          const data = res.data
          this.sightName = data.sightName
          this.bannerImg = data.bannerImg
          this.gallaryImgs = data.gallaryImgs
          this.list = data.categoryList
        }
      }
    },
    mounted(){
      this.getDetailInfo()
    }
  }
</script>

<style scoped lang="stylus">
.home
  height 50rem
</style>
