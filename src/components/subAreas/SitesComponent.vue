<template>
  <div id="sites" class="w-100 h-100 text-white d-flex justify-content-center align-items-center overflow-y-hidden">
    <div class="w-75 h-100 d-flex justify-content-between align-items-center gap-4 overflow-y-hidden">
      <div class="footerSitesElements w-50 d-flex flex-column align-items-start" v-for="(elem,index) in sitesElements">
        <h4 class="h-100 fw-semibold text-uppercase">{{ elem.title }}</h4>
        <div class="footerSitesLinks d-flex flex-column">
          <a class="fs-6" :href="link.link" v-for="link in elem.links">{{ link.text }}</a>
        </div>
      </div>
      <img src="../../assets/images/dc-logo-bg.png" alt="Logo DC">
    </div>
  </div>
</template>

<script>
  import { sitesData } from '../../data/data';
  export default {
    name: "SitesComponent",
    data(){
      return{
        sitesElements: sitesData
      }
    }
  }
</script>

<style lang="scss" scoped>
  #sites{
    height: 40vh;
    background-image: url("../../assets/images/footer-bg.jpg");
    background-size: cover;
  }
</style>