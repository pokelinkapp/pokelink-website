<script lang="ts">
import Vue from 'vue';
import quagsire from '../assets/img/quagsire.jpg';
import Twitter from '../assets/icons/twitter.svg?inline';
import Discord from '../assets/icons/discord.svg?inline';
import Patreon from '../assets/icons/patreon.svg?inline';

export default Vue.extend({
  components: {
    Twitter,
    Discord,
    Patreon,
  },
  data() {
    return {
      nav: {
        side: 'right',
        image: quagsire,
        background: '#82D5F5',
      },
    };
  },
  head() {
    return {
      title: 'Pokélink | Contact',
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
      <h1 class="sr-only">Contact us</h1>
      <ul>
        <li>
          <a
            href="https://twitter.com/PokelinkApp"
            target="_blank"
            rel="noopener noreferrer"
            title="Twitter"
            ><Twitter /> https://twitter.com/PokelinkApp</a
          >
        </li>
        <li>
          <a
            href="https://discord.pokelink.xyz"
            target="_blank"
            rel="noopener noreferrer"
            title="Discord"
            ><Discord />https://discord.pokelink.xyz</a
          >
        </li>
        <li>
          <a
            href="https://www.patreon.com/pokelink"
            target="_blank"
            rel="noopener noreferrer"
            title="Patreon"
            ><Patreon />https://www.patreon.com/pokelink</a
          >
        </li>
      </ul>
    </main>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}

li {
  margin-bottom: 50px;
}

svg {
  width: 50px;
  margin-right: 20px;
}

a {
  font-size: 20px;
  text-decoration: none;
  color: #242426;
  display: flex;
  align-items: center;

  &:hover {
    text-decoration: underline;
  }
}
</style>
