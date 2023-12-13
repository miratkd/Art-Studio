<template>
  <AppNav />
  <RouterView/>
</template>

<script>
import { RouterView } from 'vue-router';
import AppNav from './components/AppNav.vue';

export default {
  components:{
    AppNav,
    RouterView
}
}
</script>

<style>
#app {
  font-family: 'League Spartan', sans-serif;
  font-size: 1vw;
  margin: 5vh 7vw 0 7vw;
}
a{
  text-decoration: none;
}

h1 {
  color: #EEEFF4;
  font-size: 12.5em;
  font-style: normal;
  font-weight: 700;
  line-height: 0.8;
  letter-spacing: -5px;
  margin: 0;
}

h2 {
  color: #1B1D23;
  font-size: 6em;
  font-style: normal;
  font-weight: 700;
  line-height: 0.83;
  letter-spacing: -2px;
  margin: 0;
}

h3 {
  color: #1B1D23;
  font-size: 4.5em;
  font-style: normal;
  font-weight: 700;
  line-height: 0.88;
  letter-spacing: -2px;
  margin: 0;
}

h4 {
  color: #1B1D23;
  font-size: 2em;
  font-style: normal;
  font-weight: 700;
  line-height: 1.25;
  margin: 0;
}
p{
  color: #60636D;
  font-size: 1.13em;
  font-style: normal;
  font-weight: 500;
  line-height: 1.33;
  margin: 0;
}
</style>
