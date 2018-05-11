<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li v-for="item in weekendList" class="item" :key="item.id">
        <div class="item-img">
          <img :src="item.imgUrl" alt="">
        </div>
        <div class="item-mid">
          <h3>{{item.recoH3}}</h3>
          <span>{{item.recosp}}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {
        weekendList:[
          {
            id:'0001',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/ef/815eec316c47c4.jpg_r_640x214_5bf7f999.jpg',
            recoH3:'济南必游TOP10',
            recosp:'名山古寺，清泉旧巷，就是心中的济南'
          },
          {
            id:'0002',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/ef/815eec316c47c4.jpg_r_640x214_5bf7f999.jpg',
            recoH3:'济南必游TOP10',
            recosp:'名山古寺，清泉旧巷，就是心中的济南'
          },
          {
            id:'0003',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/ef/815eec316c47c4.jpg_r_640x214_5bf7f999.jpg',
            recoH3:'济南必游TOP10',
            recosp:'名山古寺，清泉旧巷，就是心中的济南'
          },
          {
            id:'0004',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/ef/815eec316c47c4.jpg_r_640x214_5bf7f999.jpg',
            recoH3:'济南必游TOP10',
            recosp:'名山古寺，清泉旧巷，就是心中的济南'
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
  border-bottom 1px solid #e0e0e0
  .item-img
    width 100%
    img
      width 100%
      height 100%
.item-mid
  padding 0 .2rem
  h3
    font-size .32rem
    margin-top .24rem
    margin-bottom .32rem
    font-weight 600
  &>span
    display block
    margin-bottom .32rem
</style>
