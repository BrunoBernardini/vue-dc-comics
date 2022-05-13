<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <ul>
        <li><a href="#">CHARACTERS</a></li>
        <li><a class="active" href="#">COMICS</a></li>
        <li><a href="#">MOVIES</a></li>
        <li><a href="#">TV</a></li>
        <li><a href="#">GAMES</a></li>
        <li><a href="#">COLLECTIBLES</a></li>
        <li><a href="#">VIDEOS</a></li>
        <li><a href="#">FANS</a></li>
        <li><a href="#">NEWS</a></li>
        <li><a href="#">SHOP</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComp"
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