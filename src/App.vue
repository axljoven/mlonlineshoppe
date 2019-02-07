<template>
  <div id="app">
    <site-header></site-header>
    <router-view/>
    <!-- <site-newsletter></site-newsletter> -->
    <site-footer></site-footer>
  </div>
</template>

<script>
import Header from './components/partials/Header.vue';
import Footer from './components/partials/Footer.vue';
import Newsletter from './components/partials/Newsletter.vue';

export default {
  name: 'App',
  components: {
    'site-header' : Header,
    'site-footer' : Footer,
    'site-newsletter' : Newsletter,
  }
}
</script>

<style>
</style>
