<template>
  <div>
    <div class="banner" @click="handleClickShow">
      <img src="http://img1.qunarzz.com/sight/p0/201405/23/9878029ca513c02652ee26bfe61a5799.jpg_600x330_d4112bfe.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">
          松兰山(AAAA景区)
        </div>
        <div class="banner-icon">
          <span class="iconfont">&#xe679;</span>&nbsp;6
        </div>
      </div>
    </div>
    <common-gallary @close="handleGallaryClose" :imgs="imgs" v-show="showGallary"></common-gallary>
  </div>
</template>

<script type="text/ecmascript-6">
import CommonGallary from 'common/gallary/gallary'
  export default {
    data() {
      return {
        showGallary:false,
        imgs:[
            'http://img1.qunarzz.com/sight/p0/201405/23/9878029ca513c02652ee26bfe61a5799.jpg_r_800x800_0c28d711.jpg',
            'http://img1.qunarzz.com/sight/p0/201405/28/3b4cc8d8638f0177e922cc643595eb20.jpg_r_800x800_14753a11.jpg'
        ]
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
      CommonGallary
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
