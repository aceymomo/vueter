<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <router-link tag="li" v-for="item in recommendMsg" class="item" :key="item.id" :to="'/detail/' + item.id">
        <div class="item-img">
          <span v-show="item.tommorw">可订明日</span>
          <img :src="item.imgUrl" alt="">
        </div>
        <div class="item-mid">
          <h3>{{item.title}}</h3>
          <span>{{item.recosp}}</span>
          <div class="item-mid-font">
            <div><span>￥</span><strong>{{item.price}}</strong>起</div>
            <div><i>{{item.address}}</i></div>
          </div>
          <button class="item-btn" type="button">{{item.print}}</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    props:{
      recommendMsg:Array
    },
    components: {

    }
  }
</script>

<style scoped lang="stylus">
@import '~styles/mixins.styl'
.recommend-title
  margin-top .2rem
  height .8rem
  line-height .8rem
  color #212121
  background #eee
  padding-left .2rem
.item
  display flex
  padding .4rem 0
  margin 0 .2rem
  border-bottom 1px solid #e0e0e0
  .item-img
    position relative
    width 2rem
    height 2rem
    span
      position absolute
      left 0
      top 0
      padding .06rem
      background #00e4e6
      border-bottom-right-radius .32rem
      color #fff
    img
      width 100%
      height 100%
.item-mid
  margin-left .2rem
  h3
    font-size .32rem
    margin-bottom .32rem
    font-weight 600
  &>span
    display block
    margin-bottom .32rem
  .item-mid-font
    margin-top .6rem
    display flex
    justify-content space-between
    span
      color #ff8300
    strong 
      color #ff8300
      font-size .4rem
  .item-btn
    font-size .24rem
    background #fff9f9
    color #f55
    margin-top .5rem
    ellipsis()
</style>
