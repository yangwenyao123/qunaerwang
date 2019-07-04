<template>
  
  <div>
    <Hheader></Hheader>
    <swiper></swiper>
    <icons></icons>
    <cakes></cakes>
    <play></play>
  </div>
</template>
<script>
import Hheader from './components/Hheader'
import swiper from './components/swiper'
import icons from './components/icons'
import cakes from './components/cakes'
import play from './components/play'
export default {
  components:{
    Hheader,
    swiper,
    icons,
    cakes,
    play
  }
}
</script>