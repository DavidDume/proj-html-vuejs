<script>
  import Header from './components/Header.vue';
  import Menu from './components/Menu.vue';
  import Main from './components/Main.vue';
  import BlogPosts from './components/BlogPosts.vue';
  import ShowTemplate from './components/ShowTemplate.vue';
  import Trailer from './components/Trailer.vue';
  import LiveDates from './components/LiveDates.vue';
  import Footer from './components/Footer.vue';

  import {store} from './store';

  export default {
    components: {
      Header,
      Menu,
      Main,
      BlogPosts,
      ShowTemplate,
      Trailer,
      LiveDates,
      Footer
    },
    data() {
      return {
        store
      }
    }
  }
</script>

<template>
  <div class="menu-container">
    <Menu v-show="store.showMenu" @closeMenu="store.showMenu = false"></Menu>
  </div>
  <div class="main-header">
    <Header @open="store.showMenu = true"></Header>
  </div>
  <div class="container">
    <Main></Main>
  </div>
  <div class="container bg-dark">
    <BlogPosts></BlogPosts>
  </div>

  <ShowTemplate title="view all latest news"></ShowTemplate>
  <Trailer></Trailer>

  <div class="container bg-dark">
    <LiveDates></LiveDates>
  </div>

  
  <ShowTemplate title="view all Live Dates"></ShowTemplate>

  <Footer></Footer>

</template>

<style lang="scss">
@use './general.scss';
@use './styles/variables' as *;

  .main-header {
    background-image: url('./assets/home_slider.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    height: 500px;
  }

  .container {
    background-color: $title-bg;
  }

  .bg-dark {
    background-color: $bg-dark;
  }
</style>
