<template>
  <div id="app">
    <div class="wrapper">
      <Header/>
      
      <main>
        <div class="sticky-top-button">
          <i class="fas fa-folder-open"></i>
          <p>Demos</p>
        </div>
        <div class="sticky-bottom-button">
          <span class="dollar">$</span><span>39</span>
          <p>On Sale</p>
        </div>
        <!-- START JUMBO ---------------------------------------------->
        <section id="jumbo">
          <div class="jumbo-text">
            <h2>Damon Vaughn</h2>
            <p>Best-selling author and the most influential public intellectual in the western world right now.</p>
            <p>- The New York Times</p>
            <div><i class="fas fa-arrow-left"></i></div>
            <div><i class="fas fa-arrow-right"></i></div>
          </div>
          <div class="buy-book">
            <img src="./assets/images/book-widget.png" alt="">
            <div class="text-buy-book">
              <h3>Latest Book Release</h3>
              <p>D. VAUGHN AUTOBIOGRAPHY</p>
              <p>Vestibulum tristique turpis in ipsum egestas lobortis. Duis maximus bibendum volutpat. Lorem ipsum dolor sit amet.</p>
            </div>
            <div class="buttons">
              <button class="buy-amazon"><i class="fab fa-amazon"></i> Buy On Amazon</button>
              <button class="buy-apple"><i class="fab fa-apple"></i> Buy On AppStore</button>
            </div>
          </div>
        </section>
        <!-- END JUMBO ------------------------------------------------>

        <!-- START MEET-THE-AUTHOR ------------------------------------>
        <section id="meet-the-author">
          <h2>More About Damon Vaughn</h2>
          <p>Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologist and the author of the multi-million copy bestseller “The story of my life.”</p>
          <button>Meet The Author</button>
        </section>
        <!-- END MEET-THE-AUTHOR -------------------------------------->

        <!-- START STORE ---------------------------------------------->
        <section id="store">
          <div class="e-commerce">
            <img v-for="(img, i) in eCommerceList" :key="i" :src="require(`./${img.image}`)" alt="">
          </div>
          <div class="latest-release">
            <img src="./assets/images/audible-app-2x-400x418.png" alt="AudibleApp">
            <div class="new-audiobook">
              <h3>New Audiobook</h3>
              <p>NO TIME TO READ? NO PROBLEM. LISTEN TO IT</p>
              <p>Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt. Maecenas eleifend congue cursus.</p>
              <img v-for="(img, i) in eCommerceColoredList" :key="i" :src="require(`./${img.colorImage}`)" alt="">
            </div>
          </div>
        </section>
        <!-- END STORE ------------------------------------------------>

        <!-- START WHAT-THE-CRITICS ----------------------------------->
        <section id="what-the-critics">
          
        </section>
        <!-- END WHAT-THE-CRITICS ------------------------------------->

        <!-- START EVENTS --------------------------------------------->
        <section id="events">
          
        </section>
        <!-- END EVENTS ----------------------------------------------->

        <!-- START NEWSLETTER ----------------------------------------->
        <section id="newsletter">
          
        </section>
        <!-- END NEWSLETTER ------------------------------------------->

        <!-- START MORE-ABOUT-AUTHOR ---------------------------------->
        <section id="more-about-author">
          
        </section>
        <!-- END MORE-ABOUT-AUTHOR ------------------------------------>

        <!-- START BLOG ----------------------------------------------->
        <section id="blog">
          
        </section>
        <!-- END BLOG ------------------------------------------------->
      </main>

      <Footer/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  },
  data() {
    return {
      eCommerceList: [
        {
          name: "ebay",
          image: "assets/images/ebay-logotan-2x-200x66.png"
        },
        {
          name: "audible",
          image: "assets/images/audible-logotan-2x-200x66.png"
        },
        {
          name: "barnes-noble",
          image: "assets/images/bb-logotan-2x-200x66.png"
        },
        {
          name: "kindle-fire",
          image: "assets/images/kindlefire-logotan-2x-200x66.png"
        }
      ],
      eCommerceColoredList: [
        {
          name: "audible",
          colorImage: "assets/images/audible-logo.png"
        },
        {
          name: "barnes-noble",
          colorImage: "assets/images/bn-logo-tall.png"
        },
        {
          name: "kindle-fire",
          colorImage: "assets/images/kindle-logo-tall.png"
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  @import './styles/general.scss';
  @import './styles/vars.scss';
  @import url('https://fonts.googleapis.com/css2?family=Kristi&display=swap');

  .wrapper {
    
    main {
      
      .sticky-top-button, .sticky-bottom-button {
        width: 65px;
        height: 65px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        position: absolute;
        z-index: 999;
        background-color: $white;
        border-radius: 10px;
        cursor: pointer;

        .fas {
          color: $tundora;
          font-size: 25px;
        }

        p {
          color: $tundora;
          font-size: 12px;
        }
      }

      .sticky-top-button {
        right: 20px;
        top: 150px;
      }

      .sticky-bottom-button {
        right: 20px;
        top: 225px;

        .dollar {
          position: absolute;
          left: 12px;
          top: 11px;
          font-size: 12px;
        }

        span {
          font-size: 25px;
          color: $keppel;
        }
      }

      #jumbo {
        display: flex;
        justify-content: flex-end;
        min-height: 100vh;
        background-image: linear-gradient(rgba(0, 0, 0, 0.1) 0%, rgba(0, 0, 0, 0.9) 100%), URL("./assets/images/hero-07-2x.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;

        .jumbo-text {
          align-self: center;
          margin-right: 200px;
          width: 800px;

          h2 {
            font-family: "Kristi";
            letter-spacing: 5px;
            font-size: 80px;
            font-weight: lighter;
            color: $saffron;
            margin: 0 0 60px 0;
          }

          p:nth-child(2) {
            color: $white;
            font-size: 48px;
            line-height: 1.4;
          }

          p:nth-child(3) {
            color: $scorpion;
            font-size: 24px;
            margin-top: 20px;
          }

          .fas {
            float: left;
            font-size: 15px;
            color: $white;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 20px;
            margin: 50px 1px 0 0;
            cursor: pointer;
          }

          .fa-arrow-left {
            border-top-left-radius: 5px;
            border-bottom-left-radius: 5px;
          }

          .fa-arrow-right {
            border-top-right-radius: 5px;
            border-bottom-right-radius: 5px;
          }
        }

        .buy-book {
          align-self: flex-end;
          background-color: $white;
          padding: 80px;
          
          img {
            float: left;
            height: 250px;
          }

          .text-buy-book {
            float: left;
            max-width: 300px;
            height: 250px;

            h3 {
              font-family: none;
              font-size: 30px;
            }

            p:nth-child(2) {
              font-weight: 600;
              color: $saffron;
              letter-spacing: 2px;
              margin: 20px 0 20px 0;
            }

            p:nth-child(3) {
              line-height: 25px;
              color: $scorpion;
            }
          }

          .buttons {
            text-align: center;

            .buy-amazon, .buy-apple {
              padding: 15px 50px 15px 50px;
              cursor: pointer;
              outline: none;
              border-radius: 0;
              border: 1px solid $fountainBlue;
              box-shadow: 0px 0px 14px -5px #51bfc7;
              background-color: $white;

              &:hover {
                transition: 0.2 linear;
                box-shadow: 0px 0px 20px -1px #51bfc7;
              }
            }

            .buy-amazon {
              border-top-left-radius: 5px;
              border-bottom-left-radius: 5px;
              border-right: none;
            }

            .buy-apple {
              border-top-right-radius: 5px;
              border-bottom-right-radius: 5px;
            }
          }
        }
      }

      #meet-the-author {
        width: 70%;
        text-align: center;
        margin: 100px auto;

        h2 {
          font-family: "Kristi";
          color: $saffron;
          font-weight: lighter;
          font-size: 80px;
        }

        p {
          margin-top: 10px;
          font-size: 30px;
          line-height: 40px;
        }

        button {
          margin-top: 50px;
          background-color: $keppel;
          border: none;
          padding: 12px 35px;
          color: $white;
          border-radius: 5px;
          font-size: 18px;
          cursor: pointer;
          transition: 0.5s ease-out;

          &:hover {
            transition: 0.2s linear;
            background-color: $blueLagoon;
          }
        }
      }

      #store {

        .e-commerce {
          background-color: $dawnPink;
          display: flex;
          justify-content: center;
          padding: 70px 0;

          img {
            padding: 0 30px;
            cursor: pointer;
          }
        }

        .latest-release {
          background-image: url("./assets/images/banner.jpg");
          background-repeat: no-repeat;
          background-size: cover;
          display: flex;
          justify-content: center;
          

          img {
            align-self: flex-end;
            margin-top: 50px;
          }

          .new-audiobook {
            width: 40%;
            align-self: center;
            text-align: center;

            h3 {
              color: $white;
              font-family: none;
              font-size: 40px;
              margin: 10px 0;
            }

            p:nth-child(2) {
              color: $saffron;
              font-size: 20px;
              margin: 15px 0;
            }

            p:nth-child(3) {
              width: 70%;
              color: $osloGray;
              font-size: 20px;
              line-height: 30px;
              margin: 10px auto 0 auto;
            }

            img {
              padding: 0 30px;
              cursor: pointer;
            }
          }
        }
      }
    }
  }
</style>
