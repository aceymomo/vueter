<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item">
        <div class="item-img">
          <span>可订明日</span>
          <img src="http://img1.qunarzz.com/sight/p0/1604/ff/ff0458e340cbfb2190.img.jpg_200x200_7796c66a.jpg" alt="">
        </div>
        <div class="item-mid">
          <h3>宁波方特东方神画</h3>
          <span>5361条评论</span>
          <div class="item-mid-font">
            <div><span>￥</span><strong>195</strong>起</div>
            <div><i>慈溪市</i></div>
          </div>
          <button class="item-btn" type="button">这里最近很火哦，好多人都在点评它呢！</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {

      }

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
