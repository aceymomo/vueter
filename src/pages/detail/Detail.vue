<template>
  <div>
    <detail-banner
      :sightName="sightName"
      :bannerImg="bannerImg"
      :bannerImgs="gallaryImgs"
    ></detail-banner>
    <detail-header></detail-header>
    <detail-contact></detail-contact>
    <div class="home">
      <detail-list :list="list"></detail-list>
    </div>
    <detail-pinglun></detail-pinglun>
    
  </div>
</template>

<script type="text/ecmascript-6">
import DetailBanner from '@/pages/detail/components/banner'
import DetailHeader from '@/pages/detail/components/Header'
import DetailList from '@/pages/detail/components/List'
import DetailContact from '@/pages/detail/components/contact'
import DetailPinglun from '@/pages/detail/components/pinglun'
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
      DetailList,
      DetailContact,
      DetailPinglun
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

</style>
