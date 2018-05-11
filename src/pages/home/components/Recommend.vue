<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li v-for="item in recommendList" class="item" :key="item.id">
        <div class="item-img">
          <span v-show="item.tommorw">可订明日</span>
          <img :src="item.imgUrl" alt="">
        </div>
        <div class="item-mid">
          <h3>{{item.recoH3}}</h3>
          <span>{{item.recosp}}</span>
          <div class="item-mid-font">
            <div><span>￥</span><strong>{{item.price}}</strong>起</div>
            <div><i>{{item.address}}</i></div>
          </div>
          <button class="item-btn" type="button">{{item.print}}</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {
        recommendList:[
          {
            id:'0001',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1604/ff/ff0458e340cbfb2190.img.jpg_200x200_7796c66a.jpg',
            recoH3:'宁波方特东方神画',
            recosp:'5361条评论',
            price:195,
            address:'慈溪市',
            print:'这里最近很火哦，好多人都在点评它呢！',
            tommorw:true
          },
          {
            id:'0002',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1604/ff/ff0458e340cbfb2190.img.jpg_200x200_7796c66a.jpg',
            recoH3:'宁波方特东方神画',
            recosp:'5361条评论',
            price:195,
            address:'慈溪市',
            print:'这里最近很火哦，好多人都在点评它呢！',
            tommorw:true
          },
          {
            id:'0003',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1604/ff/ff0458e340cbfb2190.img.jpg_200x200_7796c66a.jpg',
            recoH3:'宁波方特东方神画',
            recosp:'5361条评论',
            price:195,
            address:'慈溪市',
            print:'这里最近很火哦，好多人都在点评它呢！',
            tommorw:false
          },
          {
            id:'0004',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1604/ff/ff0458e340cbfb2190.img.jpg_200x200_7796c66a.jpg',
            recoH3:'宁波方特东方神画',
            recosp:'5361条评论',
            price:195,
            address:'慈溪市',
            print:'这里最近很火哦，好多人都在点评它呢！',
            tommorw:true
          },
        ]
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
