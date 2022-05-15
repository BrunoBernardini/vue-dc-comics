<template>
  <section>
    <ul class="container">
      <li v-for="(item, index) in menu" :key="`menu-${index}`">
        <img :src="item.src" :alt="item.name">
        <a :href="item.href">{{item.name.toUpperCase()}}</a>
      </li>
    </ul>
  </section>
</template>

<script>
import DigitalComics from "../assets/img/buy-comics-digital-comics.png";
import DCMerchandise from "../assets/img/buy-comics-merchandise.png";
import Subscription from "../assets/img/buy-comics-subscriptions.png";
import ComicShopLocator from "../assets/img/buy-comics-shop-locator.png";
import DCPowerVisa from "../assets/img/buy-dc-power-visa.svg";

export default {
  name: "ShopSection",
  data(){
    return{
      menu: [
        {
          src: DigitalComics,
          name: "Digital comics",
          href: "#"
        },
        {
          src: DCMerchandise,
          name: "DC merchandise",
          href: "#"
        },
        {
          src: Subscription,
          name: "Subscription",
          href: "#"
        },
        {
          src: ComicShopLocator,
          name: "Comic shop locator",
          href: "#"
        },
        {
          src: DCPowerVisa,
          name: "DC power visa",
          href: "#"
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars";
  section{
    height: 155px;
    background-color: $main-color;
    .container{
      justify-content: space-around;
    }
    li{
      font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
      display: flex;
      align-items: center;
      height: 35%;
      img{
        height: 100%;
        max-width: 55px;
        margin-right: 15px;
      }
      a{
        text-decoration: none;
        color: white;
        &:hover{
          text-decoration: underline;
        }
      }
    }
  }
</style>