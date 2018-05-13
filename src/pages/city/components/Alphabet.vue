<template>
  <div class="list">
    <ul>
      <li 
        @click="handleClick" class="item" 
        v-for="item of letters" 
        :key="item"
        :ref="item"
        @touchstart="handleTouchStart"
        @touchmove="handleTouchMove"
        @touchend="handleTouchEnd"
      >{{item}}</li>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  export default {
    props:{
      cities:Object
    },
    data(){
      return {
        touchStauts:false,
        stautsY:0,
        timer:null
      }
    },
    updated(){
      this.stautsY = this.$refs['A'][0].offsetTop
    },
    computed:{
      letters(){
        const letters = []
        for(let i in this.cities){
          letters.push(i)
        }
        return letters
      }
    },
    methods: {
      handleClick(e){
        this.$emit('change',e.target.innerText)
      },
      handleTouchStart(){
        this.touchStauts = true
      },
      handleTouchMove(e){
        if(this.touchStauts){
          if(this.timer){
            clearTimeout(this.timer)
          }
          this.timer = setTimeout(()=>{
            const touchY = e.touches[0].clientY - 79
            const index = Math.floor((touchY - this.stautsY) / 20)
            if(index >=0 && index <= this.letters.length){
              this.$emit('change', this.letters[index])
            }
          },16)
        }
      },
      handleTouchEnd(){
        this.touchStauts = false
      }
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
