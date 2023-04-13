<template>
  <header class="w-100 h-100 bg-white d-flex justify-content-center align-items-center">
    <div class="w-75 h-100 d-flex justify-content-between align-items-center">
      <LogoComponent />
      <div id="headerMenu" class="h-100 d-flex justify-content-between align-items-center gap-4">
        <div class="headerMenuElement h-100" v-for="(elem,index) in menuElements" :class="{'active' : elem.isActive}">
          <span class="h-100 fw-semibold text-uppercase">{{ elem.text }}</span>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
  import { menuData } from '../../data/data';
  import LogoComponent from '../single/LogoCOmponent.vue';
  export default {
    name: "HeaderComponent",
    components:{
      LogoComponent
    },
    data(){
      return{
        menuElements: menuData
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import 'bootstrap/scss/bootstrap';
  header{
    height: 15vh;
  }
  #headerMenu{
    line-height: 113px;
  }
  .headerMenuElement{
    cursor: pointer;
    border-bottom: 5px solid transparent;
    transition: all 0.1s linear;
    height: 20px;
  }
  .active, .headerMenuElement:hover{
    color: $primary;
    border-bottom: 5px solid $primary;
  }
</style>