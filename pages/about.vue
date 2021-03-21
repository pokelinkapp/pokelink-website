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
    <div>
      <h1 class="title">Pokelink about content</h1>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}
</style>
