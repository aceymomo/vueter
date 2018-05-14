<template>
  <div class="contaner" @click="handleClickClose">
    <div class="wrapper">
      <swiper :options="swiperOption">
        <!-- slides -->
        <swiper-slide v-for="(item,index) of imgs" :key="index">
          <img class="gallary-img" :src="item" alt="">
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    props:{
      imgs:{
        type:Array,
        default:[]
      }
    },
    data() {
      return {
        swiperOption:{
          pagination:'.swiper-pagination',
          paginationType:'fraction',
          observeParents:true,
          observer:true
        }
      }

    },
    methods:{
      handleClickClose(){
        this.$emit('close')
      }
    }
  }
</script>

<style scoped lang="stylus">
.contaner >>> .swiper-container
  overflow inherit
.contaner
  position fixed
  display flex
  align-items center
  z-index 99
  top 0
  left 0
  right 0
  bottom 0
  background #000
  .wrapper
    width 100%
    height 0
    padding-bottom 100%
    .gallary-img
      width 100%
      height 6rem
    .swiper-pagination
      bottom -1rem
      color:#fff
</style>
