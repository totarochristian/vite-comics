<template>
  <main class="w-100 h-100 bg-custom-black text-white d-flex justify-content-center align-items-center overflow-hidden">
    <ComicsComponent v-if="menuElements[1].isActive"/>
    <EmptyTitleComponent v-else />
  </main>
</template>

<script>
  import ComicsComponent from '../subAreas/main/ComicsComponent.vue';
  import EmptyTitleComponent from '../subAreas/main/EmptyTitleComponent.vue';
  export default {
    name: "MainComponent",
    components:{
      ComicsComponent,
      EmptyTitleComponent
    },
    props:{
      menuElements: Object
    }
  }
</script>

<style lang="scss" scoped>
  main{
    min-height: 17.7vh;
  }
</style>