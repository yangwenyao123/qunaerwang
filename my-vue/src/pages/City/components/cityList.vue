<template>
  <div class="content">
    <div class="top">
      <div class="title">
        您的位置
      </div>  
      <div class="bottom">
        <button>广州</button>
      </div>
    </div> 

    <div class="list">
      <div class="title">热门城市</div>
      <div class="time">
        <button v-for="(item,index) in city" 
        :key="index" >{{item.name}}</button> 
        
      </div>
    </div>

  </div>  

</template>
<script>
export default {
  data(){
    return {
      city:[
        {name:"广州"},
        {name:"广州"},
        {name:"广州"},
        {name:"广州"},
        {name:"广州"},
        {name:"广州"},
      ],
      active:false
    }
  },
  methods:{
     
    
     margin(){
      //  
      console.log(this.city.length );
      
      for(var i=1;i<this.city.length-1;i++){
        if(i%3==0){
          this.active = true
          console.log(this.active);
          
        }else{
          this.aa = true
          this.active = false
        }
      }
      
    }
  },
  mounted(){
   this.margin()
  },
  computd:{
    
  }
}
</script>
<style scoped>
.time{
  padding: .4rem;
}


.time button{
    width: 2.3rem;
    height: .7rem;
    line-height: .7rem;
    text-align: center;
    border: 1px solid #ccc;
    color: #000;
    background-color: #fff;
    border-radius: 2px ;
    margin:0 .2rem .3rem 0;
}

.time button:nth-child(3){
  margin-right:0
}
.time button:nth-child(6){
  margin-right:0
}
  .top{
    height: 2rem;
 
  }
 .title{
     height: .6rem;
     line-height: .6rem;
     padding-left: .4rem;
     background-color: #eee;
  
   }
  .top .bottom{
    height: 1.2rem;
    display: flex;
    align-items: center;
    padding-left: .4rem;
   
  }
  .top .bottom  button{
    width: 2.5rem;
    height: .7rem;
    line-height: .7rem;
    text-align: center;
    border: 1px solid skyblue;
    color: skyblue;
    background-color: #fff;
    border-radius: 2px ;
  
    
  }

</style>
