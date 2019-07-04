<template>
  <div class="iconlist">
    <swiper>
      <swiper-slide v-for="(page,index) in pages" :key="index">
        <div class="icon" v-for="(item,index) in page" :key="index">
          <img :src="item.icon" alt>
          <div class="text">{{item.text}}</div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        iconlist: [
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1711/df/86cbcfc533330d02.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1711/df/86cbcfc533330d02.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1611/54/ace00878a52d9702.png",
            text: "热门境地"
          },
          {
            icon:
              "http://img1.qunarzz.com/piao/fusion/1711/df/86cbcfc533330d02.png",
            text: "热门境地"
          }
        ],
        pages: []
      };
    },
    computed: {},
    methods: {
      fn() {
        const pages = [];
        this.iconlist.forEach((item, index) => {
          var index = Math.floor(index / 8);
          if (!pages[index]) {
            pages[index] = [];
          }
          pages[index].push(item);
        });
        this.pages = pages;
      }
    },

    mounted() {
      this.fn();
    }
  };
</script>
<style scoped>
  /*  */
  .swiper-slide {
    width: 100% !important;
    display: flex;
    padding: 0.3rem;
    justify-content: space-between;
    flex-wrap: wrap;
    box-sizing: border-box;
  }
  .icon {
    width: 1.2rem;
    height: 1rem;
    margin-bottom: 1rem;

    margin-right: 0.6rem;
  }
  .iconlist .icon:nth-child(4) {
    margin-right: 0;
  }
  .iconlist .icon:nth-child(8) {
    margin-right: 0;
  }

  .icon img {
    width: 100%;
    height: 100%;
    margin-bottom: 0.2rem;
  }
</style>
