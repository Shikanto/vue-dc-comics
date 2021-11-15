<template >
  <div class="card-comics-container" >
    <div class="card-comics"
      v-for="(comic, i) in dcList" :key="i">
      <img
        :src="comic.thumb"
        alt=""
      />
      <h4>{{comic.series.toUpperCase()}}</h4>
    </div>
  </div>
</template>

<script>
import jsonData from "../assets/database/dc-comics.json";

export default {
  name: "CardComics",
  data() {
    return {
      dcList: jsonData,
      infoComic:{},
    };
  },
  methods: {
      getInfoComics(comic) {
          this.infoComic = comic;
              
          },
      },
  };
 /*  mounted() {
        
            console.log(this.dcList)
        
    },*/

</script>

<style lang="scss">
@import "../style/variables";

.card-comics-container {
  display: flex;
  flex-wrap: wrap;
  gap: $gap-comics;
  padding: 60px 30px 0;
  
  .card-comics {
    flex-basis: calc(100% / 6 - $gap-comics);
    

    img {
      width: 100%;
      object-fit: cover;
      object-position:top;
      height: 55%;
    }
  }
}

h4 {
  color: white;
  font-size:20px;
  margin-top:20px;
}
</style>