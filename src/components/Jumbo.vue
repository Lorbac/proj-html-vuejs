<template>
  <section id="jumbo">
    <div class="jumbo-text">
      <h2>Damon Vaughn</h2>
      <p>Best-selling author and the most influential public intellectual in the western world right now.</p>
      <p>- The New York Times</p>
      <div><i class="fas fa-arrow-left"></i></div>
      <div><i class="fas fa-arrow-right"></i></div>
    </div>
    <div class="buy-book">
      <img src="../assets/images/book-widget.png" alt="">
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
</template>

<script>
export default {
    name: 'Jumbo',
}
</script>

<style lang="scss" scoped>

  @import '../styles/vars.scss';
  @import url('https://fonts.googleapis.com/css2?family=Kristi&display=swap');

  #jumbo {
    display: flex;
    justify-content: flex-end;
    min-height: 100vh;
    background-image: linear-gradient(rgba(0, 0, 0, 0.1) 0%, rgba(0, 0, 0, 0.9) 100%), URL("../assets/images/hero-07-2x.jpg");
    background-repeat: no-repeat;
    background-size: cover;

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
</style>