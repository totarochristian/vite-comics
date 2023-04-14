<template>
  <div id="currentSeries" class="w-75 h-100 d-flex flex-column justify-content-start align-items-start">
    <ButtonComponent title="current series" :filled="true" :size="3"/>
  </div>
</template>

<script>
  import { comicsData } from '../../data/data';
  import ButtonComponent from './ButtonComponent.vue';
  export default {
    name: "CurrentSeriesComponent",
    components: {
      ButtonComponent
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