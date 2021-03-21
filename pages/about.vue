<script lang="ts">
import Vue from 'vue';
import dratini from '../assets/img/dratini.jpg';

export default Vue.extend({
  data() {
    return {
      nav: {
        side: 'left',
        image: dratini,
        background: '#7384D6',
      },
    };
  },
});
</script>

<template>
  <div class="container">
    <Navigation
      :side="nav.side"
      :image="nav.image"
      :background="nav.background"
    />
    <main class="right">
      <h1 class="title">Pokélink.</h1>
      <p>
        An app that helps streamers & Poké-tubers create beautiful
        viewer-engaging streams when they stream/record Pokémon game
        playthroughs.
      </p>
      <p>
        It enables a bridged connection between your emulator (DeSmuME, VBA &
        Citra) and the Pokélink app; it then provides a set of browser sources
        to include in your streaming softeare. (We also allow you to manually
        control your party for non-emulated games)
      </p>
    </main>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}

h1 {
  font-size: 50px;
  font-weight: 900;
  margin-bottom: 40px;
  position: relative;

  &:before {
    content: '';
    display: block;
    height: 40px;
    width: 10px;
    position: absolute;
    left: -30px;
    top: 4px;
    background: #4d64b7;
  }
}

p {
  margin-bottom: 40px;
  font-size: 20px;
  font-weight: 100;
}
</style>
