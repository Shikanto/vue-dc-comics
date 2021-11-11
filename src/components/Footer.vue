<template>
  <footer>
    <div class="top-footer">
      <div class="container">
          <div class="list-container">
            <div class="list-footer">
              <div class="col-list">
                <h2>DC COMICS</h2>
                <ul>
                  <li v-for="(item, i) in listComics" :key="i">
                    <a :href="item.href">{{item.title}}</a>
                  </li>
                </ul>
                <h2>SHOP</h2>
                <ul>
                  <li v-for="(item, i) in listShop" :key="i">
                    <a :href="item.href">{{item.title}}</a>
                  </li>
                </ul>
              </div>
              <div class="col-list">
                <h2>DC</h2>
                <ul>
                  <li v-for="(item, i) in listDc" :key="i">
                    <a :href="item.href">{{item.title}}</a>
                  </li>
                </ul>
              </div>
              <div class="col-list">
                <h2>SITES</h2>
                <ul>
                  <li v-for="(item, i) in listSites" :key="i">
                    <a :href="item.href">{{item.title}}</a>
                  </li>
                </ul>
              </div>
            </div>
          </div>
          <div class="jumbo-logo-footer">
            <h1></h1>
          </div>
      </div>
    </div>
    <div class="bot-footer">
      <div class="container">
        <div class="sign-up">
          <a href="#">SIGN-UP NOW!</a>
        </div>
        <div class="follow-us">
            <div>
              <h2>FOLLOW US</h2>
            </div>
            <div v-for="(icon, i) in listSocial" :key="i">
              <img :src="`../assets/${icon.urlImg}`" alt="">
            </div>
            <!-- <div>
              <img src="../assets/footer-facebook.png" alt="">
            </div> -->
            

        </div>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  name:"Footer",
  data() {
    return{
      
      listComics: [
        {
          title: "Characters",
          href:"#",
        },
        {
          title: "Comics",
          href:"#",
        },
        {
          title: "Movies",
          href:"#",
        },
        {
          title: "TV",
          href:"#",
        },
        {
          title: "Games",
          href:"#",
        },
        {
          title: "Video",
          href:"#",
        },
        {
          title: "News",
          href:"#",
        }
      ],
      
      listShop:[
        {
          title: "Shop DC",
          href:"#",
        },
        {
          title: "Shop DC Collectibles",
          href:"#",
        },
      ],
      
      listDc: [
        {
          title: "Terms Of Use",
          href:"#",
        },
        {
          title: "Privacy policy (New)",
          href:"#",
        },
        {
          title: "Ad Choices",
          href:"#",
        },
        {
          title: "Advertising",
          href:"#",
        },
        {
          title: "Jobs",
          href:"#",
        },
        {
          title: "Subscriptions",
          href:"#",
        },
        {
          title: "Talent Workshops",
          href:"#",
        },
        {
          title: "CPSC Certificates",
          href:"#",
        },
        {
          title: "Ratings",
          href:"#",
        },
        {
          title: "Shop Help",
          href:"#",
        },
        {
          title: "Contact Us",
          href:"#",
        },
      ],

      listSites: [
        {
          title: "DC",
          href:"#",
        },
        {
          title: "MAD Magazine",
          href:"#",
        },
        {
          title: "DC Kids",
          href:"#",
        },
        {
          title: "DC Universe",
          href:"#",
        },
        {
          title: "DC Power Visa",
          href:"#",
        },
      ],

      listSocial:[
        {
          urlImg:"footer-facebook.png",
          alt:"Facebook Icon",
        },
        {
          urlImg:"footer-twitter.png",
          alt:"Twitter Icon",
        },
        {
          urlImg:"footer-youtube.png",
          alt:"Youtube Icon",
        },
        {
          urlImg:"footer-pinterest.png",
          alt:"Pinterest Icon",
        },
        {
          urlImg:"footer-periscope.png",
          alt:"Periscope Icon",
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

@import "../style/variables";    
    
    .top-footer{
      background-image: url("../assets/footer-bg.jpg");
      background-position: center;
      background-size: cover;
    }

    .bot-footer{
      background-color:rgb(51, 51, 51);
      padding: $padding-containers-y $padding-containers-x;

      .sign-up{
        border:4px solid $color-dc-blue;
        padding:20px;

        a{
          color:white;
          text-decoration:none;
          font-weight:bold;
          font-size:25px;
      
        }
      }

      h2{
        color:$color-dc-blue;
        margin-right:20px;
      } 
     
      
    }

    .follow-us{
      display:flex;
      justify-content:center;
      align-items:center;
      img {
        width:50px;
        height:50px;
        margin: 0 10px;
      }
    }



    .container{
      margin: 0 auto;
      width:$w-75;
      display:flex;
      justify-content:space-between;
    
    }

    .list-container{
      width:$w-40;;
    }


    .list-footer{
      display:flex;
      padding: $padding-containers-y $padding-containers-x;
    }

    .col-list{
      width:calc(100% / 3);
    }
    .jumbo-logo-footer{
      width:$w-40;
      background-image: url("../assets/dc-logo-bg.png");
      background-size: cover;
      background-position:center;
      
    }

    h2{
      color:white;
    }

    ul{
      display:flex;
      flex-direction:column;
      list-style-type:none;
      padding: 0;

      li {
        
        margin:4px 0;

        a{
        color:$text-footer;
        text-decoration:none;
        }
      }
    }

    
</style>