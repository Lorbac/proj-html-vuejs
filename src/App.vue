<template>
  <div id="app">
    <div class="wrapper">
      <Header/>
      
      <main>
        <!-- START JUMBO ---------------------------------------------->
        <section id="jumbo">

        </section>
        <!-- END JUMBO ------------------------------------------------>

        <!-- START MEET-THE-AUTHOR ------------------------------------>
        <section id="meet-the-author">

        </section>
        <!-- END MEET-THE-AUTHOR -------------------------------------->

        <!-- START STORE ---------------------------------------------->
        <section id="store">
          
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
  }
}
</script>

<style lang="scss">
  @import './styles/general.scss';
  @import './styles/vars.scss';
</style>
