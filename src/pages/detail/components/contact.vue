<template>
  <div class="contact">
    <div class="contact-box">
        <div class="contact-left">
            <div class="inner-left">
                <div class="ct-top">
                    <strong>5.0</strong>
                    <span>分</span>
                    <i>超赞</i>
                </div>
                <div class="ct-bottom">
                    <span>52833条评论</span>
                    <span>19条攻略</span>
                </div>
            </div>
            <div class="inner-right">
                <span class="iconfont">&#xe62d;</span>
            </div>
        </div>
        <div class="contact-right">
            <div class="right-left">
                <div><span>景点简介</span></div>
                <div class="right-kf">开放时间、贴士</div>
            </div>
            <div class="right-right">
                <span class="iconfont">&#xe62d;</span>
            </div>
        </div>
    </div>
    <div class="contact-bottom">
        <div class="icon">
            <span class="iconfont">&#xe636;</span>
        </div>
        <div class="contact-title">
            <span>北京市朝阳区东四环小武基北路</span>
        </div>
        <div class="contact-right">
            <span class="iconfont">&#xe62d;</span>
        </div>
    </div>
    <div class="contact-btn"></div>
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
.contact
    width 100%
    position absolute
    z-index 1
    top 4rem
    .contact-box
        border-top-left-radius .1rem
        border-top-right-radius .1rem
        background #fff
        width 100%
        display flex
        flex-wrap wrap
        .contact-left
            flex 1
            margin .2rem 0
            padding 0 .2rem
            border-right 1px solid #eee
            display flex
            align-items center
            justify-content space-between
            .inner-left
                .ct-top
                    strong
                        color #ff8300
                        font-size .44rem
                    span
                        color #ff8300
                    i
                        color #ff8300
                        margin-left .2rem
                .ct-bottom
                    margin-top .1rem
                    font-size .24rem
                    color #9e9e9e
                    span
                        margin-right .1rem
            .inner-right
                span
                    font-size 12px
        .contact-right
            flex 1
            margin .2rem 0
            padding 0 .2rem
            display flex
            align-items center
            justify-content space-between
            .right-left
                div
                    span
                        font-size .28rem
                .right-kf
                    margin-top .24rem
                    font-size .24rem
                    color #9e9e9e
    .contact-bottom
        height .8rem
        line-height .8rem
        border-top 1px solid #eee
        margin 0 .2rem
        background #fff
        display flex
        align-items center
        justify-content space-between
        .contact-title
            font-size .28rem
    .contact-btn
        width 100%
        height .2rem
        background #eee
</style>
