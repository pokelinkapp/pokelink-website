<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<template>
  <div class="container">
    <div>
      <h1 class="title">pokelink-website</h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  .title {
    color: red;
  }

  .links a {
    color: blue;
  }
}
</style>
