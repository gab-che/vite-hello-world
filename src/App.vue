<script>
  import AppTitle from "./components/AppTitle.vue";
  import AppHero from "./components/AppHero.vue";
  import AppApi from "./components/AppApi.vue";
  export default{
    components: { AppTitle, AppHero, AppApi },

    data(){
      return{
        
      }
    },

    methods: {

    }
  }
</script>

<template>
  <div class="main_container">
    <div class="container">
      <div class="row">
        <div class="col-6 m-auto">
          <AppTitle></AppTitle>
        </div>
      </div>
      <AppHero></AppHero>
      <AppApi></AppApi>
    </div>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.main_container{
  width: 90vw;
}
</style>
