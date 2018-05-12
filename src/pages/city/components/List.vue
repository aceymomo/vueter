<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title">当前城市</div>
        <div class="list-con">
          <button>北京</button>
        </div>
      </div>
      <div class="area">
        <div class="title">热门城市</div>
        <div class="list-con">
          <button v-for="item of hotCities" :key="item.id">{{item.name}}</button>
        </div>
      </div>
      <div class="area" v-for="(item,key) of cities" :key="key">
        <div class="title">{{key}}</div>
        <div class="item-city" v-for="inner of item" :key="inner.id">{{inner.name}}</div>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
import Bscroll from 'better-scroll'
  export default {
    props:{
      hotCities:Array,
      cities:Object
    },
    data() {
      return {

      }

    },
    mounted() {
      this.scroll = new Bscroll(this.$refs.wrapper)
    }
  }
</script>

<style scoped lang="stylus">
.list
  width 100%
  position absolute
  top 1.58rem
  left 0
  right 0
  bottom 0
  overflow hidden
  .area
    width 100%
    line-height .54rem
    background #eee
    .title
      color #000
      font-size .24rem
      margin 0 .3rem
    .list-con
      background #fff
      padding .04rem .2rem .2rem .2rem
      button
        padding .1rem .68rem
        border 1px solid #ccc
        border-radius .06rem
        color #000
        background none
        margin-right .1rem
        margin-top .16rem
    .item-city
      background #fff
      padding .2rem
      border-bottom 1px solid #eee
</style>
