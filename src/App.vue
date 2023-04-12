<script>
  import Header from './components/Header.vue';
  import Menu from './components/Menu.vue';

  import {store} from './store';

  export default {
    components: {
      Header,
      Menu
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

</template>

<style lang="scss">
@use './general.scss';

  .main-header {
    background-image: url('./assets/home_slider.jpg');
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    height: 600px;
  }
</style>
