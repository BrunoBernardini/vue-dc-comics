<template>
  <main>
    <div class="container">
      <h2>--> Content goes here &lt;--</h2>
    </div>
  </main>
</template>

<script>
export default {
  name: "MainComp"
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars";
  main{
    background-color: #1c1c1c;
    color: white;
    height: 132px;
    .container{
      display: flex;
      height: 100%;
      align-items: center;
    }
  }
</style>