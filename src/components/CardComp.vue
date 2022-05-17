<template>
  <div class="card">
    <div class="thumb">
      <img :src="card.thumb" :alt="`Price: ${card.price}; Type: ${card.type}`">
    </div>
    <h4>{{card.series}}</h4>
  </div>
</template>

<script>
/*
{
  "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
  "price": "$19.99",
  "series": "Action Comics",
  "type": "comic book"
},
 */
export default {
  name: "CardComp",
  props: {
    card: Object
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars";
  .card{
    width: 100%;
    font-family: $secondary-font;
    margin-bottom: 50px;
    transition: all 0.15s linear;
    cursor: pointer;
    .thumb{
      position: relative;
      overflow: hidden;
      padding-top: 100%;
      margin-bottom: 20px;
    }
    img{
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
    }
    h4{
      font-weight: 400;
      font-size: 14px;
      text-transform: uppercase;
      word-break: break-word;
    }
    &:hover{
      transform: scale(1.1);
      text-decoration: underline;
    }
  }
</style>