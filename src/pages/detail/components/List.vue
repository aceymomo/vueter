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
        <ul>
          <li class="item-box">
            <div>[夜场]北京欢乐谷成人票</div>
            <div class="item-right">
              <b class="price">￥</b>
              <strong>117.1</strong>
              <i>起</i>
              <b class="iconfont">&#xe65e;</b>
              <b class="iconfont">&#xe65d;</b>
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
  span
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
    font-size .3rem
    .item-right
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
.item-children
  padding 0 .2rem
</style>
