<template>
  <div id="contacts" class="w-100 text-white d-flex justify-content-center align-items-center overflow-hidden">
    <div class="w-75 d-flex justify-content-between align-items-center gap-4">
      <ButtonComponent title="sign-up now!" :filled="false" :size="3"/>
      <div class="d-flex justify-content-between align-items-center gap-4">
        <h5 class="text-primary fw-bold text-uppercase">follow us</h5>
        <SocialComponent />
      </div>
    </div>
  </div>
</template>

<script>
  import ButtonComponent from '../../single/ButtonComponent.vue';
  import SocialComponent from '../../single/SocialComponent.vue';
  export default {
    name: "ContactsComponent",
    components:{
      ButtonComponent,
      SocialComponent
    }
  }
</script>

<style lang="scss" scoped>
  @use 'bootstrap/scss/bootstrap' as *;
  #contacts{
    min-height: 10vh;
  }
</style>