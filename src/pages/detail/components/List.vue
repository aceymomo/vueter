<template>
  <div>
    <div class="list-title">
      <div @click="titleClick">门票<span v-show="titleshow"></span></div>
      <div @click="titleClick">一日游<span v-show="!titleshow"></span></div>
    </div>
    <ul>
      <li class="item-content">
        <span class="item-icon"></span>
        夜场票
      </li>
    </ul>
    <ul>
      <li class="item-box">
        <div class="item-left">[夜场]北京欢乐谷成人票</div>
        <div class="item-right">
          <b class="price">￥</b>
          <strong>117.1</strong>
          <i>起</i>
          <b class="iconfont">&#xe65e;</b>
          <b class="iconfont">&#xe65d;</b>
        </div>
        <ul class="item-inner-wrap">
          <li class="item-inner-box">
            <div class="inner-left">
              <span>北京欢乐谷夜场成人票(5.2-5.31)</span>
              <div class="inner-first">
                <img src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" alt="">
                <span>可订明日</span>
              </div>
              <div class="inner-second">
                <span>自营</span>
                <span>无需换票</span>
                <span>随时退</span>
              </div>
              <div class="inner-third">
                <b>去哪儿直销</b>
                <b class="inner-font">预定须知</b>
                <span class="iconfont">&#xe62d;</span>
              </div>
            </div>
            <div class="inner-right">
              <div>
                <span>￥</span>
                <strong>118.0</strong>
              </div>
              <div>
                <button>预定</button>
              </div>
            </div>
          </li>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    name:'DetailList',
    props:{
      list:Array
    },
    data() {
      return {
        titleshow:true
      }

    },
    components: {

    },
    methods:{
      titleClick(){
        this.titleshow = !this.titleshow
      }
    }
  }
</script>

<style scoped lang="stylus">
.list-title
  display flex
  height .92rem
  border-bottom 1px solid #eee
  div
    line-height .92rem
    flex 1
    text-align center
    font-size .32rem
    position relative
    span
      height 1px
      width 1.3rem
      background #00bcd4
      position absolute
      bottom 0
      left 50%
      margin-left -.65rem
.item-content
  height .88rem
  line-height .88rem
  border-bottom 1px solid #eee
  margin 0 .2rem
  &:span
    display inline-block;
    width .36rem;
    height .36rem;
    background url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat;
    margin-right .1rem;
    background-size .4rem 3rem;
    position relative
    top .06rem
    left 0
.item-box
  display flex
  justify-content space-between
  flex-wrap wrap
  font-size .3rem
  line-height .88rem
  .item-left
    margin-left .2rem
  .item-right
    margin-right .2rem
    b
      font-size .4rem
    .price
      font-size .24rem
      color #ff9800
    strong
      font-size .4rem
      color #ff9800
    i
      font-size .24rem
      color #9e9e9e
  .item-inner-wrap
    width 100%
    padding 0 .2rem
    background #f5f5f5
    .item-inner-box
      width 100%
      display flex
      line-height 1
      border-bottom 1px solid #eee
      padding .24rem 0
      .inner-left
        flex 1
        span
          font-size .28rem
          color #616161
        .inner-first
          margin-top .1rem
          img
            display inline-block
            width .2rem
            max-height .32rem
          span
            font-size .24rem
        .inner-second
          margin-top .1rem
          span
            padding .04rem
            border:1px solid #a5e4ec
            border-radius .08rem
            color #00afc7
            font-size .2rem
        .inner-third
          margin-top .1rem
          b
            font-size .24rem
            color #616161
          .inner-font
            display inline-block
            padding-left .08rem
            border-left 1px solid #bdbdbd
          span
            font-size .12rem
      .inner-right
        button
          padding .2rem
.item-children
  padding 0 .2rem
</style>
