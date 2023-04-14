<template>
  <HeaderComponent />
  <MainComponent />
  <FooterComponent />
</template>

<script>
  import HeaderComponent from "./components/mainAreas/HeaderComponent.vue";
  import MainComponent from "./components/mainAreas/MainComponent.vue";
  import FooterComponent from "./components/mainAreas/FooterComponent.vue";
  export default {
    name: "App",
    components:{
      HeaderComponent,
      MainComponent,
      FooterComponent
    }
  }
</script>

<style scoped>

</style>
