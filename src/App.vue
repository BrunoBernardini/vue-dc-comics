<template>
  <div>
    <HeaderComp/>
    <MainComp/>
    <ShopSection/>
    <FooterComp/>
  </div>
</template>

<script>
import HeaderComp from "./components/HeaderComp.vue";
import MainComp from "./components/MainComp.vue";
import ShopSection from "./components/ShopSection.vue";
import FooterComp from "./components/FooterComp.vue";

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
    ShopSection,
    FooterComp
}
}
</script>

<style lang="scss">
@import "./assets/style/general";
@import "./assets/style/mixins";
@import "./assets/style/utils";
@import "./assets/style/vars";
</style>
