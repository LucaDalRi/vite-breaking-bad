<script>
export default {
  name: 'Header',
}
</script>

<template>

  <div class="row">
    <div class="logoHeader d-flex align-items-center ms-4">
      <img src="../assets/logoyugioh.png" alt="">
      <h1>
        Yu-Gi-Oh Api
      </h1>
    </div>
  </div>

</template>

<style lang="scss" scoped>
.row {
  height: 10%;
  background-color: white;

  .logoHeader {
    height: 100%;
    width: 100%;

    img {
      height: 100%;
      width: 10%;
      object-fit: contain;
    }
  }
}
</style>