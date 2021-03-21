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
    <div>
      <h1 class="title">Pokelink home content</h1>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}
</style>
