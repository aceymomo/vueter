<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list :letter="letter" :hotCities="hotCities" :cities="cities"></city-list>
    <city-alphabet @change="handleClickLetter" :cities="cities"></city-alphabet>
  </div>
</template>

<script type="text/ecmascript-6">
import CityHeader from '@/pages/city/components/Header'
import CitySearch from '@/pages/city/components/Search'
import CityList from '@/pages/city/components/List'
import CityAlphabet from '@/pages/city/components/Alphabet'
import axios from 'axios'
  export default {
    data() {
      return {
        hotCities:[],
        cities:{},
        letter:''
      }

    },
    components: {
      CityHeader,
      CitySearch,
      CityList,
      CityAlphabet
    },
    methods:{
      getCityInfo(){
        axios.get('/api/city.json')
          .then(this.getCityInfoSuce)
      },
      getCityInfoSuce(res){
        res = res.data
        if(res.ret && res.data){
          const data = res.data
          this.hotCities = data.hotCities
          this.cities = data.cities
        }
      },
      handleClickLetter(letter){
        this.letter = letter
      }
    },
    mounted(){
      this.getCityInfo()
    }
  }
</script>

<style scoped lang="stylus">

 
</style>
