<template>
  <div id="brands" class="w-100 h-100 bg-primary text-white d-flex justify-content-center align-items-center">
    <div class="w-75 h-100 d-flex justify-content-between align-items-center gap-4">
      <div class="footerBrandElement h-100" v-for="(elem,index) in brandsElements">
        <span class="h-100 fw-semibold text-uppercase">{{ elem.text }}</span>
      </div>
    </div>
  </div>
</template>

<script>
  import { brandsData } from '../../data/data';
  export default {
    name: "BrandsComponent",
    data(){
      return{
        brandsElements: brandsData
      }
    },
    methods(){

    }
  }
</script>

<style lang="scss" scoped>
  #brands{
    min-height: 20vh;
  }
</style>