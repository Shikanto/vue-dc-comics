<template>
  <header class="container">
    <div class="navbar">
      <img src="../assets/dc-logo.png" alt="DC logo" />
      <div class="nav-links" >
        <ul>
          <li v-for="(item, i) in navbarItems" :key="i">
            <a :class="currentIndex === i ? 'active' : '' " :href="item.href">{{ item.title }}</a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      currentIndex: 1,
      navbarItems: [
        {
          title: "CHARACTERS",
          href: "#",
        },
        {
          title: "COMICS",
          href: "#",
        },
        {
          title: "MOVIES",
          href: "#",
        },
        {
          title: "TV",
          href: "#",
        },
        {
          title: "GAMES",
          href: "#",
        },
        {
          title: "CHARACTERS",
          href: "#",
        },
        {
          title: "COLLECTIBLES",
          href: "#",
        },
        {
          title: "VIDEOS",
          href: "#",
        },
        {
          title: "FANS",
          href: "#",
        },
        {
          title: "NEWS",
          href: "#",
        },
        {
          title: "SHOP",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../style/variables";
.container {
  margin: 0 auto;
  width: $w-75;
}

.nav-links {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size:0.8rem;
}

.navbar {
  display: flex;
  justify-content: space-between;
  padding: $padding-containers-y $padding-containers-x;


  ul {
    display: flex;
    justify-content: center;
    list-style-type: none;

    li a {
      padding: 10px 20px;
      text-decoration: none;
      font-weight: bold;
      display: inline-block;
      color: black;
    }
    .active{
    color: $color-dc-blue;
    border-bottom: 3px solid $color-dc-blue;  
    }
  }
}

</style>