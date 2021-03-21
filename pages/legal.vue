<script lang="ts">
import Vue from 'vue';
import ditto from '../assets/img/ditto.jpg';

export default Vue.extend({
  data() {
    return {
      nav: {
        side: 'left',
        image: ditto,
        background: '#C47BE6',
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
      <h1 class="title">Pokelink legal content</h1>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}
</style>
