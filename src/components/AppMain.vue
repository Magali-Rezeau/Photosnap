<template>
  <main>
   <section-about></section-about>
   <section-stories></section-stories>
  </main>
</template>

<script>
import SectionAbout from './SectionAbout.vue';
import SectionStories from './SectionStories.vue';
export default {
  name: 'App',
  components: {
    SectionAbout, 
    SectionStories
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

</style>
