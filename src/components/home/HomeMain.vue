<template>
  <main>
   <home-about></home-about>
   <home-stories></home-stories>
   <home-features></home-features>
  </main>
</template>

<script>
import HomeAbout from './HomeAbout.vue';
import HomeStories from './HomeStories.vue';
import HomeFeatures from './HomeFeatures.vue';
export default {
  name: 'App',
  components: {
    HomeAbout, 
    HomeStories,
    HomeFeatures,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

</style>
