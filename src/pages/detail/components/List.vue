<template>
  <div>
    <ul v-for="(item,index) of list" :key="index">
      <li class="item-content">
        <span class="item-icon"></span>
        {{item.title}}
      </li>
      <li class="item-children" v-if="item.children">
        <detail-list :list="item.children"></detail-list>
      </li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    name:'DetailList',
    props:{
      list:Array
    },
    data() {
      return {

      }

    },
    components: {

    }
  }
</script>

<style scoped lang="stylus">
.item-content
  height .88rem
  line-height .88rem
  border-bottom 1px solid #eee
  padding-left .2rem
  span
    display inline-block;
    width .36rem;
    height .36rem;
    background url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat;
    margin-right .1rem;
    background-size .4rem 3rem;
    position relative
    top .06rem
    left 0
.item-children
  padding 0 .2rem
</style>
