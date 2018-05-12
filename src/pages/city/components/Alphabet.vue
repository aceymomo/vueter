<template>
  <div class="list">
    <ul>
      <li class="item" v-for="(item,key) of cities" :key="key">{{key}}</li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    props:{
      cities:Object
    },
    components: {

    }
  }
</script>

<style scoped lang="stylus">
@import '~styles/varibles.styl'
.list
  display flex
  align-items center
  justify-content center
  position absolute
  top 1.58rem
  right 0
  bottom 0
  width .4rem
  .item
    line-height .4rem
    color $bgColor
</style>
