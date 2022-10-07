<template>
  <main>
    <div class="jumbotron"/>
    <div class="container">
      <div class="topTag">current series</div>
      <ul>
        <li
          v-for="(card, index) in cardsData"
          :key="`card-${index}`">
          <CardComp :card="card"/>
        </li>
      </ul>
      <button><h3>load more</h3></button>
    </div>
  </main>
</template>

<script>
import cardsData from "../assets/data/cardsData";
import CardComp from "./CardComp.vue";
export default {
    name: "MainComp",
    components: { CardComp },
    data(){
      return{
        cardsData
      }
    }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars";
  main{
    background-color: #1c1c1c;
    .jumbotron{
      background-image: url("../assets/img/jumbotron.jpg");
      background-position: center;
      height: 400px;
    }
    .container{
      position: relative;
      padding-top: 54px;
      color: white;
      justify-content: center;
      flex-wrap: wrap;
      ul{
        display: flex;
        flex-wrap: wrap;
        width: 100%;
        li{
          width: calc((100% / 6) - 29px);
          margin: 0 14px;
        }
      }
      button{
        color: white;
        padding: 10px 54px;
        margin-bottom: 20px;
        background-color: $main-color;
        border: none;
        font-family: $secondary-font;
        cursor: pointer;
        transition: all .15s linear;
        h3{
          font-size: 14px;
          text-transform: uppercase;
        }
        &:hover{
          background-color: lightgray;
          color: #303030;
        }
      }
    }
    .topTag{
      position: absolute;
      top: 0;
      left: 0;
      transform: translateY(-50%);
      font-size: 30px;
      font-weight: bold;
      text-transform: uppercase;
      background-color: $main-color;
      padding: 9px 17px
    }
  }
</style>