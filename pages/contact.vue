<script lang="ts">
import Vue from 'vue';
import quagsire from '../assets/img/quagsire.jpg';

export default Vue.extend({
  data() {
    return {
      nav: {
        side: 'right',
        image: quagsire,
        background: '#82D5F5',
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
      <h1 class="title">Pokelink contact content</h1>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}
</style>
