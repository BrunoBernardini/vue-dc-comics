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
          <img src="../assets/img/dc-logo-bg.png" alt="DC Logo Background">
        </div>
      </div>
    </div>
    <div class="bottom">
      <div class="container">
        <button><h3>SIGN-UP NOW!</h3></button>
        <div class="socials-container">
          <h3>FOLLOW US</h3>
          <ul>
            <li v-for="(social, index) in socials" :key="`social-${index}`">
              <a :href="social.href"><img :src="social.src" :alt="social.name"></a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Facebook from "../assets/img/footer-facebook.png";
import Twitter from "../assets/img/footer-twitter.png";
import YouTube from "../assets/img/footer-youtube.png";
import Pinterest from "../assets/img/footer-pinterest.png";
import Periscope from "../assets/img/footer-periscope.png";

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
      ],
      socials: [
        {
          name: "Facebook",
          src: Facebook,
          href: "#"
        },
        {
          name: "Twitter",
          src: Twitter,
          href: "#"
        },
        {
          name: "YouTube",
          src: YouTube,
          href: "#"
        },
        {
          name: "Pinterest",
          src: Pinterest,
          href: "#"
        },
        {
          name: "Periscope",
          src: Periscope,
          href: "#"
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/style/vars";
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
      .container{
        justify-content: space-between;
      }
      button{
        color: white;
        padding: 13px 14px;
        background-color: transparent;
        border: 2px solid $main-color;
        font-family: $secondary-font;
        cursor: pointer;
        transition: all .15s linear;
        h3{
          font-size: 17px;
        }
        &:hover{
          background-color: lightgray;
          color: #303030;
        }
      }
      .socials-container{
        display: flex;
        align-items: center;
        h3{
          font-size: 22px;
          color: $main-color;
          margin-right: 20px;
        }
        img{
          transition: all .15s linear;
          &:hover{
            transform: scale(1.2);
            filter: brightness(1.5);
          }
        }
      }
      ul{
        display: flex;
        li{
          margin: 9px;
        }
      }
    }
  }
</style>