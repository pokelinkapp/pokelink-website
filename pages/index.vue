<script lang="ts">
import Vue from 'vue';
import jolteon from '../assets/img/jolteon.jpg';

export default Vue.extend({
  data() {
    return {
      nav: {
        side: 'right',
        image: jolteon,
        background: '#FFDE53',
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
    <main class="left">
      <h1 class="title">Pokélink.</h1>
      <p>Automate & Beautified Pokémon experience.</p>
    </main>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}

h1 {
  font-size: 100px;
  font-weight: 900;
  margin-bottom: 10px;
}

p {
  font-size: 40px;
  font-weight: 100;
}
</style>
