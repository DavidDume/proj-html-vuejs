<script>
  import Header from './components/Header.vue';
  import Menu from './components/Menu.vue';
  import Main from './components/Main.vue';

  import {store} from './store';

  export default {
    components: {
      Header,
      Menu,
      Main
    },
    data() {
      return {
        store
      }
    },
    methods: {

    }
  }
</script>

<template>
  <div class="">
    <Menu v-show="store.showMenu" @closeMenu="store.showMenu = false"></Menu>
  </div>
  <div class="main-header">
    <Header @open="store.showMenu = true"></Header>
  </div>
  <div class="container">
    <Main></Main>
  </div>
  
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
</style>
