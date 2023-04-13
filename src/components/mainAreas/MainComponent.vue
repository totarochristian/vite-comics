<template>
  <main class="w-100 h-100 bg-custom-black text-white d-flex justify-content-center align-items-center">
    <div class="w-75 h-100 d-flex justify-content-between align-items-center">
      <h2>{{ title }}</h2>
    </div>
  </main>
</template>

<script>
  export default {
    name: "MainComponent",
    data(){
      return{
        title: "--> Content goes here <--"
      }
    }
  }
</script>

<style lang="scss" scoped>
  main{
    min-height: 17.7vh;
  }
</style>