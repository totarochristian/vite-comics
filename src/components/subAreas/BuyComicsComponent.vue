<template>
  <div id="brands" class="w-100 h-100 bg-primary text-white d-flex justify-content-center align-items-center">
    <div class="w-75 h-100 d-flex justify-content-around align-items-center gap-4">
      <ComicComponent :imageName="elem.imageName" :title="elem.text" v-for="elem in brandsElements" />
    </div>
  </div>
</template>

<script>
  import { brandsData } from '../../data/data';
  import ComicComponent from '../single/ComicComponent.vue';
  export default {
    name: "BuyComicsComponent",
    components:{
      ComicComponent
    },
    data(){
      return{
        brandsElements: brandsData
      }
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
  #brands{
    min-height: 20vh;
  }
</style>