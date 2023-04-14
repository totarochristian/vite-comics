<template>
  <div id="comics" class="w-100 h-100">
    <JumbotronComponent />
    <div class="w-75 h-100 d-flex justify-content-between align-items-center">

    </div>
  </div>
</template>

<script>
  import JumbotronComponent from '../../single/JumbotronComponent.vue';
  export default {
    name: "ComicsComponent",
    components:{
      JumbotronComponent
    }
  }
</script>

<style lang="scss" scoped>

</style>