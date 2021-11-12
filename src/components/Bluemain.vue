/* eslint-disable prettier/prettier */
<template>
  <div class="blue-main">
    <div class="container">
      <div class="blu-container">
        <div class="card" v-for="(item, i) in blueItems" :key="i">
          <img :src="require(`../assets/${item.urlImg}`)" :alt="item.alt" />
          <h4>{{ item.text }}</h4>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Bluemain",
  data() {
    return {
      blueItems: [
        {
          urlImg: "buy-comics-digital-comics.png",
          alt: "digital comics",
          text: "DIGITAL COMICS",
        },
        {
          urlImg: "buy-comics-merchandise.png",
          alt: "dc merchandise",
          text: "DC MERCHANDISE",
        },
        {
          urlImg: "buy-comics-subscriptions.png",
          alt: "subscription",
          text: "SUBSCRIPTION",
        },
        {
          urlImg: "buy-comics-shop-locator.png",
          alt: "digital comics",
          text: "COMIC SHOP LOCATOR",
        },
        {
          urlImg: "buy-dc-power-visa.svg",
          alt: "dc power visa",
          text: "DC POWER VISA",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables";

.blue-main {
  background-color: $color-dc-blue;
  color: white;
}

.container {
  margin: 0 auto;
  width: $w-75;
}

.blu-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: ($padding-containers-y * 2) $padding-containers-x;
}

.card {
  display: flex;
  align-items: center;
  img {
    
    width: 100px;
    height: 85px;
    padding: 0 $padding-containers-x;
  }
}
</style>
