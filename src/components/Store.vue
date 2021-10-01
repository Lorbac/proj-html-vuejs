<template>
  <section id="store">
        <div class="e-commerce">
          <img v-for="(img, i) in eCommerceList" :key="i" :src="require(`../${img.image}`)" alt="">
        </div>
        <div class="latest-release">
          <img src="../assets/images/audible-app-2x-400x418.png" alt="AudibleApp">
          <div class="new-audiobook">
            <h3>New Audiobook</h3>
            <p>NO TIME TO READ? NO PROBLEM. LISTEN TO IT</p>
            <p>Donec fringilla nunc eu turpis dignissim, at euismod sapien tincidunt. Maecenas eleifend congue cursus.</p>
            <img v-for="(img, i) in eCommerceColoredList" :key="i" :src="require(`../${img.colorImage}`)" alt="">
          </div>
        </div>
  </section>
</template>

<script>
export default {
    name: "Store",
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

<style lang="scss" scoped>

  @import '../styles/vars.scss';

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
      background-image: url("../assets/images/banner.jpg");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
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
</style>