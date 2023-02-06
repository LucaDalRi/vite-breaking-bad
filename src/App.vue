<script>
import Header from './components/AppHeader.vue';
import Navbar from './components/AppNavbar.vue'

export default {
  name: "App",
  components: {
    Header,
    Navbar,
  }
};
</script>

<template>

  <Header />
  <Navbar />

</template>

<style lang="scss">
#app {
  height: 100vh;
  width: 100vw;
  background-color: #d48f38;
}
</style>
