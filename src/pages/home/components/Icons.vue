<template>
  <div>
    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icons">
          <div v-for="item of page" :key="item.id" class="icon">
            <div class="icon-img">
              <img :src="item.imgUrl" />
            </div>
            <p>{{item.context}}</p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
  export default{
    name:'Icons',
    data(){
      return {
        iconsImg:[
          {
            id:'000001',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            context:'景点门票'
          },
          {
            id:'000002',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
            context:'自然风光'
          },
          {
            id:'000003',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/b8/c5dcdb58deec2402.png',
            context:'虎踞峡'
          },
          {
            id:'000004',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
            context:'踏青赏花'
          },
          {
            id:'000005',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
            context:'一日游'
          },
          {
            id:'000006',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/8c/47630407f70e8302.png',
            context:'横店喜剧节'
          },
          {
            id:'000007',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
            context:'游乐场'
          },
          {
            id:'000008',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/8c/47630407f70e8302.png',
            context:'影视基地'
          },
          {
            id:'000009',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/8c/47630407f70e8302.png',
            context:'影视基地'
          },
        ]
      }
    },
    computed:{
      pages(){
        const pages = []
        this.iconsImg.forEach((item,index)=>{
          const page = Math.floor(index / 8)
          if(!pages[page]){
            pages[page] = []
          } 
          pages[page].push(item)
        })
        return pages
      }
    }
  }
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons
  text-align center
  display flex
  flex-wrap wrap
  .icon
    width 25%;
    overflow hidden
    padding:.2rem 0
    .icon-img
      width 1.1rem
      height 1.1rem
      margin:0 auto
      img
        width 100%
    p
      margin-top .1rem
      color $darkColor
      ellipsis()
</style>
