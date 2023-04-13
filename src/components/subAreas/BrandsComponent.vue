<template>
  <div id="brands" class="w-100 bg-primary">

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
    }
  }
</script>

<style lang="scss" scoped>
  #brands{
    min-height: 20vh;
  }
</style>