<template>
  <div class="header">
    <router-link to="/">
      <div class="header-left">
        <span class="iconfont">&#xe624;</span>
      </div>
    </router-link>
    <div class="header-mid">城市选择</div>
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
.header
  width 100%
  height .86rem
  position relative
  background #00bcd4
  border-bottom 1px solid #fff
  .header-left
    position absolute
    left .2rem
    top 0
    width .64rem
    line-height .86rem
    color #fff
    text-align center
  .header-mid
    color #fff
    font-size .32rem
    width 100%
    line-height .86rem
    text-align center
</style>
