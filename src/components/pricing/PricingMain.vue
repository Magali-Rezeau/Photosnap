<template>
  <main>
   <pricing-about></pricing-about>
   <pricing-plan></pricing-plan>
   <pricing-features></pricing-features>
  </main>
</template>

<script>
import PricingAbout from './PricingAbout.vue';
import PricingPlan from './PricingPlan.vue';
import PricingFeatures from './PricingFeatures.vue';
export default {
  name: 'App',
  components: {
    PricingAbout, 
    PricingPlan,
    PricingFeatures,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

</style>
