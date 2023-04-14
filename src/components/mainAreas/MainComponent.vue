<template>
  <main class="w-100 h-100 bg-custom-black text-white d-flex justify-content-center align-items-center">
    <ComicsComponent />
  </main>
</template>

<script>
  import ComicsComponent from '../subAreas/main/ComicsComponent.vue';
  export default {
    name: "MainComponent",
    components:{
      ComicsComponent
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
  main{
    min-height: 17.7vh;
  }
</style>