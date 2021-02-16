<template>
  <div id="app">
    <!-- <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> -->
    <Player/>
  </div>
</template>

<script>
import Player from './components/content/player'

export default {
  components:{
    Player
  }
};
</script>
<style lang="scss">
@import "scss/index.scss";
#app {
  position: fixed;
  top: 0;
  height: 100%;
  width: 100%;
  overflow: hidden;
}
</style>
