<template>
  <div id="navigationBar" class="h-100 d-flex justify-content-between align-items-center gap-4">
    <div class="navigationBarElement h-100" v-for="(elem,index) in menuElements" :class="{'active' : elem.isActive}">
      <span class="h-100 fw-semibold text-uppercase">{{ elem.text }}</span>
    </div>
  </div>
</template>

<script>
  import { menuData } from '../../data/data';
  export default {
    name: "NavigationBarComponent",
    data(){
      return{
        menuElements: menuData
      }
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
  #navigationBar{
    line-height: 113px;
  }
  .navigationBarElement{
    cursor: pointer;
    border-bottom: 5px solid transparent;
    transition: all 0.1s linear;
    height: 20px;
  }
  .active, .navigationBarElement:hover{
    color: $primary;
    border-bottom: 5px solid $primary;
  }
</style>