<script lang="ts">
import Vue from 'vue';
import ghastly from '../assets/img/ghastly.jpg';

export default Vue.extend({
  data() {
    return {
      nav: {
        side: 'right',
        image: ghastly,
        background: '#382A39',
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
      <h1 class="title">Pokelink how it works content</h1>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}
</style>
