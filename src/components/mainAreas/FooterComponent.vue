<template>
  <footer class="bg-custom-dark d-flex flex-column justify-content-center align-items-center overflow-hidden">
    <BuyComicsComponent />
    <SitesComponent />
    <ContactsComponent />
  </footer>
</template>

<script>
  import BuyComicsComponent from '../subAreas/footer/BuyComicsComponent.vue';
  import SitesComponent from '../subAreas/footer/SitesComponent.vue';
  import ContactsComponent from '../subAreas/footer/ContactsComponent.vue';

  export default {
    name: "FooterComponent",
    components:{
      BuyComicsComponent,
      SitesComponent,
      ContactsComponent
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
  footer{
    min-height: 70vh;
  }
  @media screen and (max-width: 767.98px){
    footer{
      flex-wrap: wrap;
    }
  }
</style>