<template>
  
  <AboutComponent />
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/.vue'
import AboutComponent from '@/components/AboutComponent.vue'

export default {
  name: 'AboutView',
  components: {
    AboutComponent,
  }
}
</script>

<style>
.home{
  width: 100%;
}
</style>
