<template>
  <button type="button" class="btn text-white text-uppercase fw-bold rounded-0 btn-lg" :class="filled ? 'btn-primary' : 'btn-outline-primary'">{{ title }}</button>
</template>

<script>
  export default {
    name: "LargeButtonComponent",
    props:{
      title: String,
      filled: Boolean
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
</style>