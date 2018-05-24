<template>
  <div>
    <div class="tj-title">
        <h3>看了该景点的人还看了</h3>
    </div>
    <div class="tj-content">
        <ul>
            <li class="tj-li" v-for="item in list" :key="item.id">
                <div class="tj-img">
                    <img :src="item.img" />
                </div>
                <div class="tj-word">
                    <h3>{{item.title}}</h3>
                    <i class="iconfont" v-show="item.iconfont>0">&#xe7f1;</i>
                    <i class="iconfont" v-show="item.iconfont>1">&#xe7f1;</i>
                    <i class="iconfont" v-show="item.iconfont>2">&#xe7f1;</i>
                    <i class="iconfont" v-show="item.iconfont>3">&#xe7f1;</i>
                    <i class="iconfont" v-show="item.iconfont>4">&#xe7f1;</i>
                    <span>{{item.talk}}条评论</span>
                    <p>{{item.address}}</p>
                </div>
                <div class="tj-price">
                    <b>￥</b>
                    <strong>{{item.price}}</strong>
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
        list:[
          {
            id:1,
            img:'http://img1.qunarzz.com/sight/p0/1801/56/568ebf34301216dfa3.img.jpg_228x168_e02586ed.jpg',
            title:'北京活的3D博物馆',
            iconfont:5,
            talk:556,
            address:'北京朝阳区',
            price:35
          },
          {
            id:2,
            img:'http://img1.qunarzz.com/sight/p0/1608/4f/4fc3f5a1b838f279a3.water.jpg_228x168_f8ba8013.jpg',
            title:'北京杜莎夫人蜡像馆',
            iconfont:5,
            talk:6074,
            address:'北京前门大街',
            price:39
          },
          {
            id:3,
            img:'http://img1.qunarzz.com/sight/p0/1501/40/40b2b6c951b28fdd.water.jpg_228x168_cafb44f3.jpg',
            title:'水立方',
            iconfont:4,
            talk:3138,
            address:'北京奥林匹克公园',
            price:14
          },
          {
            id:4,
            img:'http://img1.qunarzz.com/sight/p0/1602/68/68aa05adb5315f9990.water.jpg_228x168_3aee83cc.jpg',
            title:'北京海洋馆',
            iconfont:2,
            talk:1506,
            address:'北京西城区',
            price:170
          },
          {
            id:5,
            img:'http://img1.qunarzz.com/sight/p0/201308/08/41150dacc0e3a0c8c8d65eac.jpg_228x168_837c0639.jpg',
            title:'北京动物园',
            iconfont:3,
            talk:1087,
            address:'北京西城区',
            price:39.9
          },
          {
            id:6,
            img:'http://img1.qunarzz.com/sight/p0/1602/67/67feeab24cfc82bb90.water.jpg_228x168_a8d0ede5.jpg',
            title:'太平洋海底世界',
            iconfont:5,
            talk:4396,
            address:'北京海淀区',
            price:66
          },
        ]
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
        padding .2rem 0
        border-bottom 1px solid #eee
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
            font-size 0
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
