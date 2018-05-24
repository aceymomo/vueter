<template>
  <div>
    <div class="tj-title">
        <h3>看了该景点的人还看了</h3>
    </div>
    <div class="tj-content">
        <ul>
            <li class="tj-li">
                <div class="tj-img">
                    <img src="http://img1.qunarzz.com/sight/p0/1801/56/568ebf34301216dfa3.img.jpg_228x168_e02586ed.jpg" />
                </div>
                <div class="tj-word">
                    <h3>北京活的3D博物馆</h3>
                    <i class="iconfont">&#xe7f1;</i>
                    <i class="iconfont">&#xe7f1;</i>
                    <i class="iconfont">&#xe7f1;</i>
                    <i class="iconfont">&#xe7f1;</i>
                    <i class="iconfont">&#xe7f1;</i>
                    <span>556条评论</span>
                    <p>北京●朝阳区</p>
                </div>
                <div class="tj-price">
                    <b>￥</b>
                    <strong>35</strong>
                    <span>起</span>
                </div>
            </li>
        </ul>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {

      }

    },
    components: {

    },
  }
</script>

<style scoped lang="stylus">
.tj-title
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
.tj-content
    padding .2rem .2rem
    .tj-li
        display flex
        .tj-img
            width 2.4rem
            height 1.62rem
            img
                width 100%
                height 100%
        .tj-word
            margin-left .2rem
            font-size 0
            flex 1
            h3
                font-size .3rem
                color #212121
                margin-bottom .4rem
            i
                font-size .24rem
                color #ffb436
            span
                font-size .24rem
                color #9e9e9e
                margin-left .3rem
            p
                margin-top .3rem
                font-size .24rem
                color #9e9e9e
        .tj-price
            margin-right auto
            b
                font-size .24rem
                color #ff9800
            strong
                font-size .36rem
                color #ff9800
            span
                font-size .24rem
                color #9e9e9e
</style>
