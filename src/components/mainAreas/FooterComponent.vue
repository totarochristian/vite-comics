<template>
  <footer class="bg-custom-dark d-flex flex-column justify-content-center align-items-center">
    <BrandsComponent />
    <SitesComponent />
    <ContactsComponent />
  </footer>
</template>

<script>
  import BrandsComponent from '../subAreas/BrandsComponent.vue';
  import SitesComponent from '../subAreas/SitesComponent.vue';
  import ContactsComponent from '../subAreas/ContactsComponent.vue';

  export default {
    name: "FooterComponent",
    components:{
      BrandsComponent,
      SitesComponent,
      ContactsComponent
    }
  }
</script>

<style lang="scss" scoped>
  footer{
    min-height: 70vh;
  }
</style>