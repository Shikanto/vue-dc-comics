<template>
  <div class="div-main">
    <div class="container">
      <div class="jumbotron"></div>
    </div>
  </div>
</template>

<script>
//import jsonData from "../assets/dc-comics.json";

export default {
  name: "Main",
  /* data() {
      dcList: jsonData;
  } */
};
</script>

<style lang="scss" scoped>
@import "../style/variables";

.div-main {
  background-color: $bg-dark;
}

.container {
  margin: 0 auto;
  width: $w-75;
  background-color: black;

  .jumbotron {
    padding: ($padding-containers-y * 2) $padding-containers-x;
  }
}
h1 {
  color: white;
}
</style>