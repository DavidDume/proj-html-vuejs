<script>
  import Header from './components/Header.vue';

  export default {
    components: {
      Header
    }
  }
</script>

<template>
  <div class="main-header">
    <Header></Header>
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
