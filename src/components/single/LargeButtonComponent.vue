<template>
  <button type="button" class="btn btn-outline-primary text-white text-uppercase fw-bold rounded-0 btn-lg">{{ title }}</button>
</template>

<script>
  export default {
    name: "LargeButtonComponent",
    props:[
      "title"
    ]
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
</style>