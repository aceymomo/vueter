<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="home"></div>
  </div>
</template>

<script type="text/ecmascript-6">
import DetailBanner from '@/pages/detail/components/banner'
import DetailHeader from '@/pages/detail/components/Header'
  export default {
    name:"Detail",
    data() {
      return {

      }

    },
    components: {
      DetailBanner,
      DetailHeader
    }
  }
</script>

<style scoped lang="stylus">
.home
  height 50rem
</style>
