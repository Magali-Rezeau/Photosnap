<template>
  <div id="app">
    <app-header></app-header>
    <app-main></app-main>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
  }
}
</script>

<style lang="scss">
:root {
  $fs-xs: .75rem;
  $fs-s: .8125rem;
  $fs-m: .9375rem;
  $fs-l: 1.125rem;
  $fs-xl: 2rem;
  $fw-regular: 400;
  $fw-bold: 700;
}
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body {
  font-size: 12px;
  font-family: 'DM Sans', sans-serif;
}
ul {
  list-style: none;
}
a {
  text-decoration: none;
  color: black;
  text-transform: uppercase;
}
.btn {
  background-color: black;
  color: white;
  width: 19.375rem;
  height: 3rem;
  text-transform: uppercase;
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
