<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <ul>
        <li v-for="(option, index) in menu" :key="`menu-${index}`">
          <a :class="{'active':option.isActive}" :href="option.href">{{option.name.toUpperCase()}}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComp",
  data(){
    return{
      menu: [
        {
          name: "characters",
          href: "#",
          isActive: false,
        },
        {
          name: "comics",
          href: "#",
          isActive: true,
        },
        {
          name: "movies",
          href: "#",
          isActive: false,
        },
        {
          name: "tv",
          href: "#",
          isActive: false,
        },
        {
          name: "games",
          href: "#",
          isActive: false,
        },
        {
          name: "collectibles",
          href: "#",
          isActive: false,
        },
        {
          name: "videos",
          href: "#",
          isActive: false,
        },
        {
          name: "fans",
          href: "#",
          isActive: false,
        },
        {
          name: "news",
          href: "#",
          isActive: false,
        },
        {
          name: "shop",
          href: "#",
          isActive: false,
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars";
  header{
    height: 118px;
    background-color: aliceblue;
    font-size: 14px;
    .container{
      display: flex;
      height: 100%;
      justify-content: space-between;
      align-items: center;
    }
    .logo{
      width: 80px;
    }
    ul{
      list-style: none;
      display: flex;
      height: 100%;
      a{
        display: inline-flex;
        align-items: center;
        height: 100%;
        color: rgb(70, 70, 70);
        text-decoration: none;
        margin: 0 16px;
        border-bottom: 6px solid transparent;
        font-weight: 500;
        &:hover,
        &.active{
          border-bottom: 6px solid $main-color;
          color: $main-color;
        }
      }
    }
  }
</style>