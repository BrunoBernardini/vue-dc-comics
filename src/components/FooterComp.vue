<template>
  <footer>
    <div class="top">
      <div class="container">
        <div class="footer-list">
          <h3>DC COMICS</h3>
          <ul>
            <li>Characters</li>
            <li>Comics</li>
            <li>Movies</li>
            <li>TV</li>
            <li>Games</li>
            <li>Videos</li>
            <li>News</li>
          </ul>
        </div>
        <div class="footer-list">
          <h3>SHOP</h3>
          <ul>
            <li>Shop DC</li>
            <li>Shop DC Collectibles</li>
          </ul>
        </div>
        <div class="footer-list">
          <h3>DC</h3>
          <ul>
            <li>Terms Of Use</li>
            <li>Privacy policy (New)</li>
            <li>Ad Choices</li>
            <li>Advertising</li>
            <li>Jobs</li>
            <li>Subscriptions</li>
            <li>Talent Workshops</li>
            <li>CPSC Certificates</li>
            <li>Ratings</li>
            <li>Shop Help</li>
            <li>Contact Us</li>
          </ul>
        </div>
        <div class="footer-list">
          <h3>Sites</h3>
          <ul>
            <li>DC</li>
            <li>MAD Magazine</li>
            <li>DC Kids</li>
            <li>DC Universe</li>
            <li>DC Power Visa</li>
          </ul>
        </div>
      </div>
    </div>
    <div class="bottom"></div>
  </footer>
</template>

<script>
export default {
  name: "FooterComp"
}
</script>

<style lang="scss" scoped>
  footer{
    color: white;
    .top{
      height: 370px;
      padding: 40px 0;
      background-image: url("../assets/img/footer-bg.jpg");
      background-size: cover;
      .container{
        flex-direction: column;
        align-items: flex-start;
        align-content: flex-start;
        justify-content: left;
        flex-wrap: wrap;
      }
      h3{
        font-size: 22px;
        margin-bottom: 13px;
      }
      ul{
        margin: 0 27px 17px 0;
        font-size: 14px;
        li{
          margin-bottom: 3px;
          color: gray;
        }
      }
    }
    .bottom{
      height: 110px;
      background-color: #303030;
    }
  }
</style>