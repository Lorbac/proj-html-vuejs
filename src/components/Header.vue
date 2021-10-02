<template>
  <header>
    <div class="logo">
      <img src="../assets/images/author-logo-round-small.png" alt="logo">
    </div>
    <div class="nav-bar">
      <ul>
        <li :class="(link.current) ? 'active' : 'null'" v-for="(link, index) in links" :key="index">
          <a :class="(link.current) ? 'active' : 'null'" v-html="link.text" :href="link.url"></a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      links: [
        {
          text: "Home",
          url: "#",
          current: true
        },
        {
          text: "About Me",
          url: "#",
          current: false
        },
        {
          text: "Testimonials",
          url: "#",
          current: false
        },
        {
          text: "My Blog",
          url: "#",
          current: false
        },
        {
          text: "Meetups",
          url: "#",
          current: false
        },
        {
          text: "Shop",
          url: "#",
          current: false
        },
        {
          text: "Contact Me",
          url: "#",
          current: false
        },
        {
          text: "<i class='fas fa-shopping-cart'></i>",
          url: "#",
          current: false
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import '../styles/vars.scss';
  @import '~@fortawesome/fontawesome-free/css/all.min.css';

  header {
    display: flex;
    justify-content: space-between;
    position: absolute;
    width: 100%;
    z-index: 999;
    background-color: rgba (255,255,255,0);

    .logo {
      width: 30%;
      padding: 10px 0 0 70px;
      
      img {
        width: 25%;
        cursor: pointer;
      }
    }

    .nav-bar {
      width: 70%;
      display: flex;
      justify-content: flex-end;
      padding-right: 100px;

      ul {
        list-style: none;
        display: flex;

        li {
          padding-top: 50px;
          margin-left: 50px;

          &:hover,
          &.active {
            border-top: 5px solid $anzac;
            padding-top: 45px;
            transition-duration: 100ms;
          }

          &:hover a,
          &.active a {
            color: $anzac;
            transition-duration: 100ms;
          }

          a {
            text-decoration: none;
            color: $white;

          }
        }
      }
    }
  }
</style>
