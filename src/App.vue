<script>
import Header from './components/AppHeader.vue';

export default {
  name: "App",
  components: {
    Header,
  }
};
</script>

<template>

  <Header />

</template>

<style lang="scss">
#app {
  height: 100vh;
  width: 100vw;
  background-color: #d48f38;
}
</style>
