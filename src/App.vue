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

        <MoreAboutTheAuthor/>

        <Blog/>

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
import MoreAboutTheAuthor from './components/MoreAboutAuthor.vue';
import Blog from './components/Blog.vue'
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
    MoreAboutTheAuthor,
    Blog,
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
