<template>
  <div class="wrapper">
    <div class="logo">
      <img src="../assets/images/author-logo-round-200x205.png" alt="">
    </div>
    <div class="container">
      <div class="aboutMe">
        <h3>ABOUT ME</h3>
        <p>Vivamus suscipit tortor eget felis porttitor volutpat. Nulla quis lorem ut libero malesuada feugiat. Vivamus suscipit tortor eget felis porttitor volutpat.</p>
      </div>
      <div class="usefullLinks">
        <h3>USEFULL LINKS</h3>
        <ul>
          <li v-for="(link, index) in links" :key="index">
            <a :href="link.url">
              {{ link.name }}
            </a>
          </li>
        </ul>
      </div>
      <div class="contactInfo">
        <h3>CONTACT INFO</h3>
        <ul>
          <li v-for="(info, index) in info" :key="index">
            {{info}}
          </li>
        </ul>
        <div class="social">
          <a v-for="(social, index) in social" :key="index" v-html="social.logo" :href="social.url"></a>
        </div>
      </div>
    </div>
    <div class="copyright">
      <p>© Copyright 2021 | Boolean | All Rights Reserved | Powered by Lorenzo Baccini</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      links: [
        {
          name: "Latest Books",
          url:"#"
        },
        {
          name: "Upcoming Events",
          url:"#"
        },
        {
          name: "Recent Articles",
          url:"#"
        },
        {
          name: "Business Enquiries",
          url:"#"
        },
        {
          name: "Visit My Foundation",
          url:"#"
        }
      ],
      info: {
        addres: "63 E. Studebaker Street Bolingbrook, IL 60440",
        phone: "Phone: (800) 000-0000",
        mobile: "Mobile: (800) 000-0000",
        email: "Email: info@your-company.com",
      },
      social: [
        {
          logo: "<i class='fab fa-facebook-f'></i>",
          url: "#"
        },
        {
          logo: "<i class='fab fa-twitter'></i>",
          url: "#"
        },
        {
          logo: "<i class='fab fa-instagram'></i>",
          url: "#"
        },
        {
          logo: "<i class='fab fa-linkedin-in'></i>",
          url: "#"
        },
        {
          logo: "<i class='fab fa-youtube'></i>",
          url: "#"
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  @import '../styles/vars.scss';

  .wrapper {
    background-image: linear-gradient(rgba(0, 0, 0, 0.1) 0%, rgba(0, 0, 0, 0.9) 100%), url("../assets/images/hero-07-2x.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
    display: flex;
    flex-direction: column;

    .logo {
      position: absolute;
      top: 100px;
      left: 80px;
    }

    .container {
      width: 60%;
      margin: 0 auto;
      display: flex;
      justify-content: center;

      .aboutMe, .usefullLinks, .contactInfo {
        flex-basis: calc(100% / 3);
        padding: 80px 40px;
      }

      h3 {
        font-family: none;
        color: $white;
        margin: 40px 0;
      }

      .aboutMe {
        
        p {
          color: $pumice;
          line-height: 30px;
        }
      }
  
      .usefullLinks {
        margin-left: 40px;
        
        ul {
          list-style: none;

          li {
            padding: 8px 0;

            &::before {
              content: "";
              display: inline-block;
              height: 0.9em;
              width: 0.9em;
              background-image: url("../assets/images/chevron-right-solid.svg");
              background-size: contain;
              background-repeat: no-repeat;
              padding-right: 10px;
              vertical-align: middle;
            }

            a {
              text-decoration: none;
              color: $pumice;
              font-size: 15px;

              &:hover {
                color: $saffron;
                transition: 300ms linear;
              }
            }
          }
        }
      }
  
      .contactInfo {
        
        ul {
          list-style: none;

          li {
            color: $pumice;
            line-height: 30px;
          }
        }

        .social {
          margin-top: 20px;
          a {
            color: $white;
            padding: 10px 20px 10px 0;
            font-size: 20px;
          }
        }
      }
    }

    .copyright {
      margin: 0 auto;
      color: $pumice;
      font-size: 15px;
      margin-bottom: 50px;
    }
  }
</style>