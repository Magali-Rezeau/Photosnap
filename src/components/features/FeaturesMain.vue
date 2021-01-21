<template>
  <main>
   <features-about></features-about>
   <features-section></features-section>
   <app-link></app-link>
  </main>
</template>

<script>
import FeaturesAbout from './FeaturesAbout.vue';
import FeaturesSection from './FeaturesSection.vue';
import AppLink from './../AppLink.vue';
export default {
  name: 'App',
  components: {
    FeaturesAbout, 
    FeaturesSection,
    AppLink,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

</style>
