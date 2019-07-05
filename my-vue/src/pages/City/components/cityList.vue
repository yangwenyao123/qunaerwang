<template>
<div>
  <div class="content" ref="cityList">
    <div>
      <div class="top">
        <div class="title">您的位置</div>
        <div class="bottom">
          <button>广州</button>
        </div>
      </div>

      <div class="list">
        <div class="title">热门城市</div>
        <div class="time">
          <button v-for="(item,index) in hotCities" :key="index">{{item.name}}</button>
        </div>
      </div>
      <div class="cityList">
        <div class="tiem" v-for="(item,key) in cities" :key="key" :ref="key">
          <div class="title">{{key}}</div>
          <ul>
            <li v-for="(item,index) in item" :key="index">{{item.name}}</li>
         
          </ul>
        </div>
      
      </div>
    </div>
  </div>
 
</div>
</template>
<script>

import Bscroll from "better-scroll";
export default {
  props:{
    hotCities:Array,
    cities:Object,
    letter:String
  },

    data() {
      return {
        city: [
          { name: "广州" },
          { name: "广州" },
          { name: "广州" },
          { name: "广州" },
          { name: "广州" },
          { name: "广州" }
        ]
      };
    },
    mounted() {
      this.scroll = new Bscroll(this.$refs.cityList);
    },
    watch: {
      letter () {
        if(this.letter){
            var element = this.$refs[this.letter][0]
            this.scroll.scrollToElement(element)
        
        }
      
      }
    }
    
  };
</script>
<style scoped>
  .content {
    position: absolute;
    top: 2rem !important;
    bottom: 0;
    right: 0;
    overflow: hidden;
  }

  .cityList li {
    height: 0.8rem;
    border-bottom: 1px solid #ccc;
    line-height: 0.8rem;
    padding-left: 0.4rem;
  }
  .time {
    padding: 0.4rem;
  }

  .time button {
    width: 2.3rem;
    height: 0.7rem;
    line-height: 0.7rem;
    text-align: center;
    border: 1px solid #ccc;
    color: #000;
    background-color: #fff;
    border-radius: 2px;
    margin: 0 0.2rem 0.3rem 0;
  }

  .time button:nth-child(3) {
    margin-right: 0;
  }
  .time button:nth-child(6) {
    margin-right: 0;
  }
  .top {
    height: 2rem;
  }
  .title {
    height: 0.6rem;
    line-height: 0.6rem;
    padding-left: 0.4rem;
    background-color: #eee;
  }
  .top .bottom {
    height: 1.2rem;
    display: flex;
    align-items: center;
    padding-left: 0.4rem;
  }
  .top .bottom button {
    width: 2.5rem;
    height: 0.7rem;
    line-height: 0.7rem;
    text-align: center;
    border: 1px solid skyblue;
    color: skyblue;
    background-color: #fff;
    border-radius: 2px;
  }
</style>
