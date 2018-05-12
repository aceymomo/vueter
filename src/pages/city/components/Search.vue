<template>
  <div class="search">
    <input type="text" placeholder="输入城市名或拼音" />
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
@import '~styles/varibles.styl'
.search
  height .72rem
  background $bgColor
  padding 0 .1rem
  input
    box-sizing border-box
    width 100%
    height .62rem
    padding 0 .1rem
    line-height .62rem
    text-align center
    border-radius .06rem
    color #666
</style>
