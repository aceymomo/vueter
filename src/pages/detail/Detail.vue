<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="home">
      <detail-list :list="list"></detail-list>
    </div>
    
  </div>
</template>

<script type="text/ecmascript-6">
import DetailBanner from '@/pages/detail/components/banner'
import DetailHeader from '@/pages/detail/components/Header'
import DetailList from '@/pages/detail/components/List'
  export default {
    name:"Detail",
    data() {
      return {
        list:[
          {
            title:'去哪儿推荐',
            children:[
              {
                title:'宁波方特东方神话成人票',
                children:[
                  {
                    title:'成人三馆联票'
                  }
                ]
              },
              {
                title:'宁波方特东方神话儿童票'
              },
            ]
          },
          {
            title:'门票'
          },
        ]
      }

    },
    components: {
      DetailBanner,
      DetailHeader,
      DetailList
    }
  }
</script>

<style scoped lang="stylus">
.home
  height 50rem
</style>
