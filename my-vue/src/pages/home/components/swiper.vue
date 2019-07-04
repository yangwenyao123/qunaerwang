<template>
  <swiper :options="swiperOption" ref="mySwiper">
    <!-- slides -->
    <swiper-slide v-for="(item,index) in swiperImg" :key="index">
      <img class="swiper-img" :src="item.img" alt="">
    </swiper-slide>
    
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</template>
<script>
export default {
   data() {
      return {
        swiperOption: {
          // pagination:".swiper-pagination"
      pagination: {
          el: '.swiper-pagination',
        },
          // some swiper options/callbacks
          // 所有的参数同 swiper 官方 api 参数
          // ..
        },
        swiperImg:[
          {
           id:1,
            img:"http://img5.imgtn.bdimg.com/it/u=1457704519,3529830056&fm=26&gp=0.jpg"
          }, 
           {
           id:1,
            img:"http://pic25.nipic.com/20121205/10197997_003647426000_2.jpg"
          }, 
           {
           id:1,
            img:"http://pic25.nipic.com/20121205/10197997_003647426000_2.jpg"
          }, 
           {
           id:1,
            img:"http://img5.imgtn.bdimg.com/it/u=1457704519,3529830056&fm=26&gp=0.jpg"
          }, 
        ]
      }
    },
}
</script>

<style>
    .swiper-pagination-bullet-active{
     background: #fff !important;
   }
   .swiper-img{ 
     width: 100%;
     height: 3.2rem;
   }

  

</style>