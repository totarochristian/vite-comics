<template>
  <main class="w-100 h-100 bg-custom-black text-white d-flex justify-content-center align-items-center">
    <div class="w-75 h-100 d-flex justify-content-between align-items-center">
      <EmptyTitleComponent />
    </div>
  </main>
</template>

<script>
  import EmptyTitleComponent from '../subAreas/main/EmptyTitleComponent.vue';
  export default {
    name: "MainComponent",
    components:{
      EmptyTitleComponent
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
  main{
    min-height: 17.7vh;
  }
</style>