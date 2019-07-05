<template>
  <div>
    <Hheader :city="city"></Hheader>
    <swiper :swiperList="swiperList"></swiper>
    <icons :iconList="iconList"></icons>
    <cakes :recommendList="recommendList"></cakes>
    <play :weekendList="weekendList"></play>
  </div>
</template>
<script>
  import Hheader from "./components/Hheader";
  import swiper from "./components/swiper";
  import icons from "./components/icons";
  import cakes from "./components/cakes";
  import play from "./components/play";
  export default {
    data() {
      return {
        iconList: [],
        recommendList: [],
        swiperList: [],
        weekendList: [],
        city:"广州"
      };
    },
    components: {
      Hheader,
      swiper,
      icons,
      cakes,
      play
    },
    methods: {
      axios() {
        this.$axios.get("/api/index.json").then(res => {
          console.log(res);
          
          var data = res.data.data;
          this.iconList = data.iconList;
          this.recommendList = data.recommendList;
          this.swiperList = data.swiperList;
          this.weekendList = data.weekendList;
        
        });
      }
    },
    mounted() {
      this.axios();
    }
  };
</script>