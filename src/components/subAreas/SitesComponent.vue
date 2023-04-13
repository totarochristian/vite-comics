<template>
  <div id="sites" class="w-100 text-white d-flex justify-content-center align-items-center overflow-hidden">
    <div class="w-75 d-flex justify-content-between align-items-center gap-4">
      <div class="col-4 p-4 d-flex justify-content-between flex-wrap gap-1">
        <SiteComponent :list="list" v-for="list in sitesElements" />
      </div>
      <img src="../../assets/images/dc-logo-bg.png" alt="Logo DC">
    </div>
  </div>
</template>

<script>
  import { sitesData } from '../../data/data';
  import SiteComponent from '../single/SiteComponents.vue';
  export default {
    name: "SitesComponent",
    components:{
      SiteComponent
    },
    data(){
      return{
        sitesElements: sitesData
      }
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
  #sites{
    height: 40vh;
    background-image: url("../../assets/images/footer-bg.jpg");
    background-size: cover;
  }
</style>