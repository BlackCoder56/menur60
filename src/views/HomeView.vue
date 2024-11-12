<template>
  <div class="home">
    <HomeComponent />
  </div>
  <div class="about">
    <AboutComponent />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/.vue'
import HomeComponent from '@/components/HomeComponent.vue'
import AboutComponent from '@/components/AboutComponent.vue'

export default {
  name: 'HomeView',
  components: {
    HomeComponent,
    AboutComponent,
  }
}
</script>

<style>
.home{
  width: 100%;
  padding-bottom: 35px;
}

.about{
  /* background-color: red; */
  width: 100%;
}
</style>
