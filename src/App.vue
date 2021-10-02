<template>
  <div id="app">
    <div class="wrapper">
      
      <Header/>
      
      <main>
        <FixedButtons/>

        <Jumbo/>

        <MeetTheAuthor/>

        <Store/>

        <WhatTheCritics/>

        <Events/>

        <Newsletter/>

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
import Header from './components/Header.vue';
import FixedButtons from './components/FixedButtons.vue';
import Jumbo from './components/Jumbo.vue';
import MeetTheAuthor from './components/MeetTheAuthor.vue';
import Store from './components/Store.vue';
import WhatTheCritics from './components/WhatTheCritics.vue';
import Events from './components/Events.vue';
import Newsletter from './components/Newsletter.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    FixedButtons,
    Jumbo,
    MeetTheAuthor,
    Store,
    WhatTheCritics,
    Events,
    Newsletter,
    Footer,
  },
}
</script>

<style lang="scss">
  @import './styles/general.scss';
  @import './styles/vars.scss';

  .wrapper {
    
    main {
      
    }

  }
</style>
