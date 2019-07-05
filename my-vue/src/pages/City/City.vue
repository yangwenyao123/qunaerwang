<template>
  <div class="content">
    <cityH></cityH>
    <cityList></cityList>
  </div>
</template>
<script>
  import cityH from './components/cityHeader'
  import cityList from './components/cityList'
  export default {
    data () {
      return {

      }
    },
    components:{
      cityH,
      cityList
    }
  }
</script>
