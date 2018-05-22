<template>
  <div class="header">
    <router-link to="/">
      <div class="abs" v-show="showAbs">
        <span class="iconfont">&#xe624;</span>
      </div>
    </router-link>
    <transition name="fade">
      <div @click="goHome" class="fixed" v-show="!showAbs">
        <span class="iconfont">&#xe624;</span>
        宁波方特东方神话
      </div>
    </transition>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    data() {
      return {
        showAbs:true
      }

    },
    components: {

    },
    methods:{
      handleaaScroll(){
        const top = document.documentElement.scrollTop
        if(top > 60){
          this.showAbs = false
        }else{
          this.showAbs = true
        }
      },
      goHome(){
        this.$router.push('/')
      }
    },
    mounted(){
      window.addEventListener('scroll',this.handleaaScroll)
    },
    unmounted(){
      window.removeEventListener('scroll',this.handleaaScroll)
    }
  }
</script>

<style scoped lang="stylus">
.fade-enter
  opacity 0
.fade-enter-active,.fade-leave-active
  transition all 0.5s
.fade-leave-to
  opacity 0
.header
  margin-bottom 2.1rem
  .abs
    position absolute
    left .2rem
    top .04rem
    width .8rem
    height .8rem
    border-radius .4rem
    background rgba(0,0,0,.8)
    display flex
    justify-content center
    align-items center
    span
      color #fff
  .fixed
    z-index 2
    position fixed
    top 0
    left 0
    right 0
    width 100$
    line-height .88rem
    text-align center
    font-size .32rem
    color #fff
    background #00bcd4
    span
      position absolute
      left .2rem
      top .04rem
      width .8rem
      height .8rem
      display flex
      justify-content center
      align-items center
</style>
