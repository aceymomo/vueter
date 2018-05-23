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
        <div @click="handleClickList">
          <div class="item-left">[夜场]北京欢乐谷成人票</div>
          <div class="item-right">
            <b class="price">￥</b>
            <strong>117.1</strong>
            <i>起</i>
            <b class="iconfont" v-show="!listshow">&#xe65e;</b>
            <b class="iconfont" v-show="listshow">&#xe65d;</b>
          </div>
        </div>
        <ul class="item-inner-wrap" v-show="listshow" ref="inner">
          <li class="item-inner-box" v-for="(item,index) in listlist" :key="item.id" :class="{active:index<classIndex}">
            <div class="inner-left">
              <span>{{item.title}}</span>
              <div class="inner-first">
                <img src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" alt="">
                <span v-show="item.today">可订明日</span>
              </div>
              <div class="inner-second">
                <span v-show="item.ziying">自营</span>
                <span v-show="item.huanpiao">无需换票</span>
                <span v-show="item.suishi">随时退</span>
                <span v-show="item.tiaojian">条件退</span>
              </div>
              <div class="inner-third">
                <b>{{item.fangshi}}</b>
                <b class="inner-font">预定须知</b>
                <span class="iconfont">&#xe62d;</span>
              </div>
            </div>
            <div class="inner-right">
              <div class="inner-right-top">
                <span>￥</span>
                <strong>{{item.price}}</strong>
              </div>
              <div>
                <button>预定</button>
              </div>
            </div>
          </li>
          <div class="listshows" @click="hindleClicksy" v-show="classIndex == 2">
            <strong>查看剩余报价</strong>
            <span class="iconfont">&#xe65e;</span>
          </div>
        </ul>
      </li>
    </ul>
    <div class="bttom"></div>
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
        titleshow:true,
        listshow:false,
        classIndex:2,
        listlist:[
          {
            id:1,
            title:'北京欢乐谷夜场成人票(5.2-5.31)',
            today:true,
            ziying:true,
            huanpiao:true,
            suishi:true,
            tiaojian:false,
            fangshi:'去哪儿直销',
            price:118.0
          },
          {
            id:2,
            title:'北京欢乐谷夜场成人票(5.2-5.31)',
            today:true,
            ziying:false,
            huanpiao:true,
            suishi:false,
            tiaojian:true,
            fangshi:'驴妈妈旅游网',
            price:118.0
          },
          {
            id:3,
            title:'【刷身份证入园，无需换票】北京欢乐谷夜场成人票',
            today:true,
            ziying:false,
            huanpiao:true,
            suishi:false,
            tiaojian:true,
            fangshi:'先行旅游网',
            price:117.1
          },
          {
            id:4,
            title:'【刷身份证入园，无需换票】北京欢乐谷夜场成人票',
            today:true,
            ziying:false,
            huanpiao:true,
            suishi:false,
            tiaojian:true,
            fangshi:'票票券',
            price:118.0
          },
          {
            id:5,
            title:'【刷身份证入园，无需换票】北京欢乐谷夜场成人票',
            today:true,
            ziying:false,
            huanpiao:false,
            suishi:true,
            tiaojian:false,
            fangshi:'蓝精灵',
            price:118.0
          },
        ]
      }
    },
    components: {
    },
    methods:{
      titleClick(){
        this.titleshow = !this.titleshow
      },
      handleClickList(){
        this.listshow = !this.listshow
      },
      hindleClicksy(){
        this.classIndex = this.$refs.inner.length - 1
      }
    },
    computed:{

    },
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
  font-size .3rem
  line-height .88rem
  &>div
    display flex
    justify-content space-between
    flex-wrap wrap
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
    background #f5f5f5
    .item-inner-box
      width 100%
      display flex
      align-items center
      line-height 1
      border-bottom 1px solid #eee
      padding .24rem .2rem
      &.active
        display none
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
        margin-right .4rem
        .inner-right-top
          display flex
          justify-content center
          align-items flex-end
          span
            font-size .18rem
            color #ff9800
          strong
            font-size .4rem
            color #ff9800
        button
          padding .14rem .58rem
          border-radius .08rem
          color #fff
          background-image linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%)
    .listshows
      display flex
      justify-content center
      background #fff
      font-size .28rem
      strong 
        margin-right .1rem
.item-children
  padding 0 .2rem
.bttom
  height .2rem
  background #eee
  width 100%
</style>