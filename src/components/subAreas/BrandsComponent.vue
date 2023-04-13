<template>
  <div id="brands" class="w-100 h-100 bg-primary text-white d-flex justify-content-center align-items-center">
    <div class="w-75 h-100 d-flex justify-content-around align-items-center gap-4">
      <div class="footerBrandElement d-flex gap-2 align-items-center" v-for="(elem,index) in brandsElements">
        <img :src="GetImagePath(elem.imageName)" :alt="elem.text">
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
    methods: {
      GetImagePath(imageName){
        return new URL("../../assets/images/"+imageName,import.meta.url).href;
      }
    }
  }
</script>

<style lang="scss" scoped>
  #brands{
    min-height: 20vh;
  }
  #brands img {
    width: 65px;
    height: 65px;
    object-fit: contain;
  }
</style>