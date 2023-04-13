<template>
  <div id="contacts" class="w-100 text-white d-flex justify-content-center align-items-center overflow-hidden">
    <div class="w-75 d-flex justify-content-between align-items-center gap-4">
      <LargeButtonComponent title="sign-up now!" />
      <div class="d-flex justify-content-between align-items-center gap-4">
        <h5 class="text-primary fw-bold text-uppercase">follow us</h5>
        <div id="socials" class="d-flex gap-3">
          <a :href="social.link" v-for="social in socialElements">
            <img :src="GetImagePath(social.imageName)" :alt="social.name">
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { socialsData } from '../../data/data';
import LargeButtonComponent from '../single/LargeButtonComponent.vue';
  export default {
    name: "ContactsComponent",
    components:{
      LargeButtonComponent
    },
    data(){
      return{
        socialElements: socialsData
      }
    },
    methods: {
      GetImagePath(imageName){
        return new URL("../../assets/images/"+imageName,import.meta.url).href;
      }
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
  #contacts{
    min-height: 10vh;

    a{
      &:hover img{
        filter: brightness(0) invert(1);
      }
    }
  }
</style>