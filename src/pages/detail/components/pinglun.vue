<template>
  <div>
    <div class="pl-title">
      <h3>用户评论</h3>
    </div>
    <div class="pl-content" v-for="item in list" :key="item.id">
      <div class="pl-top">
        <div class="slide">
          <span class="iconfont" v-show="item.titleSlide>0">&#xe7f1;</span>
          <span class="iconfont" v-show="item.titleSlide>1">&#xe7f1;</span>
          <span class="iconfont" v-show="item.titleSlide>2">&#xe7f1;</span>
          <span class="iconfont" v-show="item.titleSlide>3">&#xe7f1;</span>
          <span class="iconfont" v-show="item.titleSlide>4">&#xe7f1;</span>
        </div>
        <div>
          <b>{{item.user}}</b>
          <b>{{item.date}}</b>
        </div>
      </div>
      <div class="pl-ct">
        <p :class="{hovers:soshow}">{{item.content}}</p>
      </div>
      <div class="pl-show" @click="handleClickshow">
        <span class="iconfont" v-show="!soshow">&#xe65e;</span>
        <span class="iconfont" v-show="soshow">&#xe65d;</span>
      </div>
      <div class="pl-img">
        <ul>
          <li v-for="(items,index) in item.img" :key="index"><img :src="items" /></li>
          <div class="clear"></div>
          <div class="img-num">共{{item.img.length}}张</div>
        </ul>
      </div>
    </div>
    <div class="pl-all">
      <strong>查看全部评论</strong>
      <span class="iconfont">&#xe62d;</span>
    </div>
    <div class="pl-bttom"></div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {
        soshow:false,
        list:[
          {
            id:1,
            titleSlide:5,
            user:'m**0',
            date:'2018-01-24',
            content:'首先，团购价格比较便宜。日常学生票就100，这个季节确实有好多项目没开，但100肯定超值了。一些很刺激的项目也是有的，太阳神车和黄色过山车都可以，爱琴海主题里的项目都开了，就因为淡季所以没什么人排队，两个电影体验也比较好。淡季也有淡季的好处，特洛伊木马我很刺激但没去尝试。入园很快很方便，查完身份证学生证就直接刷身份证进去了，挺好的，园里有好多流浪的猫猫在香格里拉那个主题区，喜欢猫猫的朋友可以带一点猫粮去喂它们。',
            img:[
              'https://imgs.qunarzz.com/piao/fusion/1801/47/f988f3961facbd02.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/5d/d30bc60cf33b8602.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/ca/2ded090b25805402.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/a3/3880c7d008820c02.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/f8/9a3bce48cf2abd02.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/dc/9aef6fc6779de902.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/3e/32f2a455ed0f4902.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/f6/e8a32e27f4587302.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/50/ad3992a354b1ce02.jpg'
            ]
          },
          {
            id:2,
            titleSlide:3,
            user:'s**2',
            date:'2018-02-16',
            content:'首先，团购价格比较便宜。日常学生票就100，这个季节确实有好多项目没开，但100肯定超值了。一些很刺激的项目也是有的，太阳神车和黄色过山车都可以，爱琴海主题里的项目都开了，就因为淡季所以没什么人排队，两个电影体验也比较好。淡季也有淡季的好处，特洛伊木马我很刺激但没去尝试。入园很快很方便，查完身份证学生证就直接刷身份证进去了，挺好的，园里有好多流浪的猫猫在香格里拉那个主题区，喜欢猫猫的朋友可以带一点猫粮去喂它们。',
            img:[
              'https://imgs.qunarzz.com/piao/fusion/1801/ca/2ded090b25805402.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/a3/3880c7d008820c02.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/f8/9a3bce48cf2abd02.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/dc/9aef6fc6779de902.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/3e/32f2a455ed0f4902.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/f6/e8a32e27f4587302.jpg',
              'https://imgs.qunarzz.com/piao/fusion/1801/50/ad3992a354b1ce02.jpg'
            ]
          }
        ]
      }

    },
    components: {

    },
    methods:{
      handleClickshow(){
        this.soshow = !this.soshow
      }
    }
  }
</script>

<style scoped lang="stylus">
.clear
  clear both
.pl-title
  font-size .3rem
  line-height .88rem
  border-bottom 1px solid #eee
  padding 0 .4rem
  h3
    position relative
    &:after
      content " "
      position absolute
      top .33rem
      left -.2rem
      width .06rem
      height .25rem
      background #1ba9ba
.pl-content
  padding 0 .2rem .46rem
  border-bottom 1px solid #eee
  .pl-top
    margin-top .1rem
    line-height .6rem
    display flex
    justify-content space-between
    .slide
      font-size 0
      span
        font-size .24rem
        color #ffb436
    b
      margin-left .1rem
      font-size .24rem
  .pl-ct
    p
      height 105px
      overflow hidden
      font-size .26rem
      line-height .42rem
      color #616161
      &.hovers
        height auto
        overflow auto
  .pl-show
    line-height .48rem
    text-align center
  .pl-img
    width 100%
    position relative
    height 3.36rem
    overflow hidden
    li
      float left
      width 2.2rem
      height 1.6rem
      margin-right .16rem
      margin-bottom .16rem
      img
        width 100%
        height 100%
    .img-num
      position absolute
      right 0
      bottom .2rem
      padding .1rem .4rem
      background rgba(0,0,0,.6)
      border-radius .2rem
      color #fff
.pl-all
  display flex
  height .8rem
  line-height .8rem
  color #616161
  justify-content center
  strong
    font-weight normal
    font-size .28rem
  span
    font-size .2rem
    margin-left .1rem
.pl-bttom
  height .2rem
  width 100%
  background #eee
</style>
