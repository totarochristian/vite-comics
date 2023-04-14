<template>
  <div id="currentSeries" class="w-75 h-100 d-flex flex-column justify-content-start align-items-start">
    <LargeButtonComponent title="current series" :filled="true"/>
  </div>
</template>

<script>
  import { comicsData } from '../../data/data';
  import LargeButtonComponent from './LargeButtonComponent.vue';
  export default {
    name: "CurrentSeriesComponent",
    components: {
      LargeButtonComponent
    },
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
    margin-top: -1.7rem;
  }
</style>