<template>
  <div>
    <div class="banner" @click="handleClickShow">
      <img :src="bannerImg" alt="">
      <div class="banner-info">
        <div class="banner-title">
          {{this.sightName}}
        </div>
        <div class="banner-icon">
          <span class="iconfont">&#xe679;</span>&nbsp;{{this.bannerImgs.length}}
        </div>
      </div>
    </div>
    <fade-animation>
      <common-gallary @close="handleGallaryClose" :imgs="bannerImgs" v-show="showGallary"></common-gallary>
    </fade-animation>
  </div>
</template>

<script type="text/ecmascript-6">
import CommonGallary from 'common/gallary/gallary'
import FadeAnimation from 'common/fade/Fade'
  export default {
    props:{
      sightName:String,
      bannerImg:String,
      bannerImgs:Array
    },
    data() {
      return {
        showGallary:false,
      }

    },
    methods:{
      handleClickShow(){
        this.showGallary = true
      },
      handleGallaryClose(){
        this.showGallary = false
      }
    },
    components: {
      CommonGallary,
      FadeAnimation
    }
  }
</script>

<style scoped lang="stylus">
.banner
  overflow hidden
  height 0
  padding-bottom 55%
  position relative
  img
    width 100%
  .banner-info
    position absolute
    left 0
    bottom 0
    width 100%
    display flex
    background-image linear-gradient(rgba(0,0,0,0),rgba(0,0,0,.8))
    .banner-title
      flex 1
      color #fff
      line-height .4rem
      font-size .32rem
      padding-left .2rem
      margin-bottom .4rem
    .banner-icon
      padding 0 .4rem
      margin-right .2rem
      height .4rem
      line-height .4rem
      border-radius .2rem
      background rgba(0,0,0,.6)
      color #fff
      span
        font-size .16rem
</style>
