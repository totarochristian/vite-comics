<template>
  <div id="contacts" class="w-100 text-white d-flex justify-content-center align-items-center overflow-hidden">
    <div class="w-75 d-flex justify-content-between align-items-center gap-4">
      <button type="button" class="btn btn-outline-primary text-white text-uppercase fw-bold rounded-0 btn-lg">sign-up now!</button>
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
  export default {
    name: "ContactsComponent",
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
#contacts{
  min-height: 10vh;

  a{
    &:hover img{
      filter: brightness(0) invert(1);
    }
  }
}
</style>