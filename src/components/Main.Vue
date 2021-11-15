<template>
  <div class="div-main">
    <div class="jumbotron">
    </div>
    <div class="container">
      <div class="series">
        <h1>CURRENT SERIES</h1>
      </div>
      <CardComics/>
      <div class="loadBtn"> 
        <a >LOAD MORE</a>
      </div>
    </div>
  </div>
</template>

<script>


import CardComics from './CardComics.vue';


export default {
  name: "Main",
  components: {
    CardComics,
  },
  
};
</script>

<style lang="scss" scoped>
@import "../style/variables";

.div-main {
  background-color: $bg-dark;

  .jumbotron {
    padding: ($padding-containers-y * 2) $padding-containers-x;
    background-image: url("../assets/jumbotron.jpg");
    height: 500px;
    background-repeat: no-repeat;
    background-size: cover;
  }

  .container {
    margin: 0 auto;
    width: $w-75;
    position: relative;

    .series{
      background-color:$color-dc-blue;
      color: white;
      padding: 10px 30px;
      display: inline-block;
      position: absolute;
      top: 0;
      transform: translateY(-50%);
      
      
    }
  }

  .loadBtn {

    text-align: center;
    padding-bottom: $padding-containers-y;

    a{
    background-color: $color-dc-blue;
    color: white;
    padding: 10px 60px;
    font-size:1.5rem;
    }
  }
}
</style>