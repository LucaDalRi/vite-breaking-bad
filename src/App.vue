<script>
import Header from './components/AppHeader.vue';
import Navbar from './components/AppNavbar.vue';
import Main from './components/AppMain.vue'

export default {

  data() {
    return {
    }
  },
  name: "App",
  components: {
    Header,
    Navbar,
    Main,
  }
};
</script>

<template>

  <Header />
  <Navbar />
  <Main />

</template>

<style lang="scss">
#app {
  width: 100vw;
  background-color: #d48f38;
}
</style>
