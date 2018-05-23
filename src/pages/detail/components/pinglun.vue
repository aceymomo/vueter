<template>
  <div>
    <div class="pl-title">
      <h3>用户评论</h3>
    </div>
    <div class="pl-content">
      <div class="pl-top">
        <span class="iconfont">&#xe7f1;</span>
        <div>
          <b>m*0</b>
          <b>2018-01-24</b>
        </div>
      </div>
      <div class="pl-ct">
        <p :class="{hovers:soshow}">首先，团购价格比较便宜。日常学生票就100，这个季节确实有好多项目没开，但100肯定超值了。
一些很刺激的项目也是有的，太阳神车和黄色过山车都可以，爱琴海主题里的项目都开了，就因为淡季所以没什么人排队，两个电影体验也比较好。淡季也有淡季的好处，特洛伊木马我很刺激但没去尝试。
入园很快很方便，查完身份证学生证就直接刷身份证进去了，挺好的，园里有好多流浪的猫猫在香格里拉那个主题区，喜欢猫猫的朋友可以带一点猫粮去喂它们。</p>
      </div>
      <div class="pl-show" @click="handleClickshow">
        <span class="iconfont" v-show="!soshow">&#xe65e;</span>
        <span class="iconfont" v-show="soshow">&#xe65d;</span>
      </div>
      <div class="pl-img">
        <ul>
          <li><img src="" alt=""></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {
        soshow:false
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
.pl-title
  font-size .3rem
  line-height .88rem
  border-bottom 1px solid #eee
  padding 0 .4rem
  h3
    position relative
    &:after
      content:" "
      position absolute
      top .33rem
      left -.2rem
      width .06rem
      height .25rem
      background #1ba9ba
.pl-content
  padding 0 .2rem
  .pl-top
    margin-top .1rem
    line-height .6rem
    display flex
    justify-content space-between
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
</style>
