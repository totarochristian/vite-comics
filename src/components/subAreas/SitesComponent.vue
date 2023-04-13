<template>
  <div id="sites" class="w-100 text-white d-flex justify-content-center align-items-center overflow-hidden">
    <div class="w-75 d-flex justify-content-between align-items-center gap-4">
      <div id="footerSitesElements" class="col-4 p-4 d-flex justify-content-between flex-wrap gap-1">
        <div class="d-flex flex-column justify-content-start align-items-start" v-for="(elem,index) in sitesElements">
          <h5 class="fw-semibold text-uppercase">{{ elem.title }}</h5>
          <div class="footerSitesLinks d-flex flex-column">
            <a class="fs-7 text-capitalize" :href="link.link" v-for="link in elem.links">{{ link.text }}</a>
          </div>
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

    a{
      text-decoration: none;
      color: grey;
      &:hover{
        color: white;
        text-decoration: underline;
      }
    }
  }
</style>