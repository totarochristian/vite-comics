<template>
  <div id="currentSeries" class="w-75 h-100 d-flex justify-content-between align-items-center">
    
  </div>
</template>

<script>
  import { comicsData } from '../../data/data';
  export default {
    name: "CurrentSeriesComponent",
    data(){
      return{
        currentSeriesComics: comicsData
      }
    }
  }
</script>

<style lang="scss" scoped>
  #currentSeries{
    min-height: 60vh;
  }
</style>