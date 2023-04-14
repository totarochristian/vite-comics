<template>
  <div :id="'comic_'+index" class="comic d-flex flex-column">
    <div class="comicImage">
      <img :src="comicData.thumb" :alt="comicData.series" class="w-100 h-100">
    </div>
    <p class="w-100 text-uppercase pt-3">{{ comicData.series }}</p>
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
  $squareSize: 210px;
  .comic{
    width: $squareSize;
    .comicImage{
      width: 100%;
      height: $squareSize;
      img{
        object-fit: cover;
      }
    }
  }
</style>