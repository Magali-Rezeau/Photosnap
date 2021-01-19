<template>
  <div id="app">
    <app-header></app-header>
    <!-- <home-main></home-main> -->
    <pricing-main></pricing-main>
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
// import HomeMain from "./components/home/HomeMain.vue";
import PricingMain from "./components/pricing/PricingMain.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  name: "App",
  components: {
    AppHeader,
    // HomeMain,
    PricingMain,
    AppFooter,
  },
};
</script>

<style lang="scss" scroped>
@mixin sm {
  @media (min-width: 600px) {
      @content;
  }
}
@mixin md {
  @media (min-width: 900px) {
      @content;
  }
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-size: 12px;
  font-family: "DM Sans", sans-serif;
}
ul {
  list-style: none;
}
a {
  cursor: pointer;
  text-decoration: none;
  color: black;
  text-transform: uppercase;
  
}
.btn {
  cursor: pointer;
  background-color: black;
  color: white;
  width: 19.375rem;
  height: 3rem;
  text-transform: uppercase;
  font-size: 15px;
  line-height: 20px;
  transition: all .5s;
  @include sm {
    width: 9.875rem;
    height: 2.5rem;
    font-size: 12px;
    line-height: 16px;
    letter-spacing: 2px;
  }
  &:hover {
     background-color:  #DFDFDF;
  color: black;
  }
}
button {
  cursor: pointer;

}
figure {
  width: 100%;
  height: 100%;
}
img {
  display: block;
  width: 100%;
  height: 100%;
}
button {
  border: none;
  background-color: transparent;
}
</style>
