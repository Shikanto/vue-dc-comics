<template>
  <div id="app">
    <Header></Header>
    <Main></Main>
    <Bluemain></Bluemain>
    <Footer></Footer>
  </div>
</template>

<script>
//qui importiamo i componenti
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Bluemain from "./components/Bluemain.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Bluemain,
    Footer
  },
};
</script>

<style lang="scss">
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
</style>
