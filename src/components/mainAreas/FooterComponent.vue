<template>
  <footer class="bg-custom-dark d-flex flex-column justify-content-center align-items-center">
    <BuyComicsComponent />
    <SitesComponent />
    <ContactsComponent />
  </footer>
</template>

<script>
  import BuyComicsComponent from '../subAreas/BuyComicsComponent.vue';
  import SitesComponent from '../subAreas/SitesComponent.vue';
  import ContactsComponent from '../subAreas/ContactsComponent.vue';

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
</style>