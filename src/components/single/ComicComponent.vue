<template>
  <div :id="'comic_'+index" class="comic">
    <p>{{ comicData.series }}</p>
  </div>
</template>

<script>
  export default {
    name: "ComicComponent",
    props:{
      index: Number,
      comicData: Object
    }
  }
</script>

<style lang="scss" scoped>
  .comic{
    width: 100% / 6;
  }
</style>