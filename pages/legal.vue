<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  mounted() {
    this.$nuxt.$emit('page', 'legal');
  },
});
</script>

<template>
  <div class="container">
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
