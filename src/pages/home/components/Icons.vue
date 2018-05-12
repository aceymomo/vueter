<template>
  <div>
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icons">
          <div v-for="item of page" :key="item.id" class="icon">
            <div class="icon-img">
              <img :src="item.imgUrl" />
            </div>
            <p>{{item.desc}}</p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
  export default{
    name:'Icons',
    props:{
      iconMsg:Array
    },
    data(){
      return {
        swiperOption:{
          autoplay:false
        }
      }
    },
    computed:{
      pages(){
        const pages = []
        this.iconMsg.forEach((item,index)=>{
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
