<template>
  <footer>
    <div class="top">
      <div class="container">
        <div class="lists-container">
          <div v-for="(list, index) in lists" :key="`list-${index}`">
            <h3>{{list.listName.toUpperCase()}}</h3>
            <ul>
              <li v-for="(option, index2) in list.options" :key="`option-${index2}`">
                <a :href="option.href">{{option.optName}}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="logo-container">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>
    <div class="bottom"></div>
  </footer>
</template>

<script>
export default {
  name: "FooterComp",
  data(){
    return{
      lists: [
        {
          listName: "Dc Comics",
          options: [
            {
              optName: "Characters",
              href: "#"
            },
            {
              optName: "Comics",
              href: "#"
            },
            {
              optName: "Movies",
              href: "#"
            },
            {
              optName: "TV",
              href: "#"
            },
            {
              optName: "Games",
              href: "#"
            },
            {
              optName: "Videos",
              href: "#"
            },
            {
              optName: "News",
              href: "#"
            }
          ]
        },
        {
          listName: "Shop",
          options: [
            {
              optName: "Shop DC",
              href: "#"
            },
            {
              optName: "Shop DC Collectibles",
              href: "#"
            }
          ]
        },
        {
          listName: "Dc",
          options: [
            {
              optName: "Terms Of Use",
              href: "#"
            },
            {
              optName: "Privacy policy (New)",
              href: "#"
            },
            {
              optName: "Ad Choices",
              href: "#"
            },
            {
              optName: "Advertising",
              href: "#"
            },
            {
              optName: "Jobs",
              href: "#"
            },
            {
              optName: "Subscriptions",
              href: "#"
            },
            {
              optName: "Talent Workshops",
              href: "#"
            },
            {
              optName: "CPSC Certificates",
              href: "#"
            },
            {
              optName: "Ratings",
              href: "#"
            },
            {
              optName: "Shop Help",
              href: "#"
            },
            {
              optName: "Contact Us",
              href: "#"
            }
          ]
        },
        {
          listName: "Sites",
          options: [
            {
              optName: "DC",
              href: "#"
            },
            {
              optName: "MAD Magazine",
              href: "#"
            },
            {
              optName: "DC Kids",
              href: "#"
            },
            {
              optName: "DC Universe",
              href: "#"
            },
            {
              optName: "DC Power Visa",
              href: "#"
            }
          ]
        }
      ]
    }
  }
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
      overflow: hidden;
      .container{
        justify-content: space-between;
      }
      .lists-container{
        height: 100%;
        width: 56%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        align-content: flex-start;
        justify-content: left;
        flex-wrap: wrap;
      }
      .logo-container{
        width: 44%;
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
        }
        a{
          color: gray;
          text-decoration: none;
          &:hover{
            text-decoration: underline;
          }
        }
      }
    }
    .bottom{
      height: 110px;
      background-color: #303030;
    }
  }
</style>