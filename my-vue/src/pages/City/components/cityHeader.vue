<template>
  <div class="content">
    <div class="header">
      <div class="top">
        
        <div class="le">
          <router-link to="/">
            <i class="iconfont">&#xe606;</i>
          </router-link>
        </div>
        <div class="right">
          <div class="tab">
            <div class="left active">境内</div>
            <div class="ri">国际/地区</div>
          </div>
        </div>
      </div>
      <div class="bottom">
        <input type="text" placeholder="请输入城市或清音">
      </div>
    </div>
  </div>
</template>
<style scoped>
  .header{
    height: 2rem;
    background-color: skyblue;
     padding-left: .2rem;
     padding-right: .2rem;
  }
  .top {
    height: 50%;
    display: flex;
    align-items: center;
    color: #fff;
  }
   .top .le{
     width: 2rem;
     display: flex;
     align-items: center;
    
   }
   .le a{
     color: #fff;
   }
   .top .right{
     
     display: flex;
     align-items: center;
   }
   .top  .tab{
     width: 4.5rem;
     height: .7rem;
     
      border: 1px solid #fff;
     line-height: .7rem;
     display: flex;
     text-align: center;
   }
    .top .tab .left{
      text-align: center;
      width: 50%;
    }
     .top .tab .ri{
     text-align: center;
      width: 50%;
    }
    .active {
      background-color: #fff;
      color: skyblue;
    }
    .bottom{
      display: flex;
      align-items: center;
      height: 50%;
    }
    input{
      width: 100%;
      height: .7rem;
      text-align: center;
    }

</style>
