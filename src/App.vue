<template>
  <div id="app">
    <app-head></app-head>
    <keep-alive>
      <router-view></router-view>
    </keep-alive>
    <player></player>
  </div>
</template>

<script>
  import AppHead from '@/common/Head.vue'
  import Player from '@/components/player/Player'
  export default {
    name: 'app',
    components: {
      AppHead,
      Player
    }
  }
</script>

<style lang="scss">
  @import "sass/app";

  body.jay-theme::before {
    position: fixed;
    background-image: url("./assets/bg.png");
    background-repeat: no-repeat;
    background-position: 50%;
    background-size: cover;
    content: '';
    height: 100%;
    top: 0;
    left: 0;
    z-index: -1;
    width: 100%;
  }
  .app-content{
    position: fixed;
    width: 100%;
    top: 88px;
    bottom: 0;
    .warpper {
      height: 100%;
      overflow: hidden;
    }
  }
</style>
