<script>
import Vue from 'vue';
import jolteon from '../assets/img/jolteon.jpg';
import dratini from '../assets/img/dratini.jpg';
import ditto from '../assets/img/ditto.jpg';
import ghastly from '../assets/img/ghastly.jpg';
import quagsire from '../assets/img/quagsire.jpg';

const pagePokemon = Object.freeze({
  home: {
    side: 'right',
    image: jolteon,
    background: '#FFDE53',
  },
  about: {
    side: 'left',
    image: dratini,
    background: '#7384D6',
  },
  how: {
    side: 'right',
    image: ghastly,
    background: '#382A39',
  },
  legal: {
    side: 'left',
    image: ditto,
    background: '#C47BE6',
  },
  contact: {
    side: 'right',
    image: quagsire,
    background: '#82D5F5',
  },
});

export default Vue.extend({
  data() {
    return {
      pokemon: pagePokemon.home,
    };
  },
  created() {
    this.$nuxt.$on('page', (data) => {
      this.pokemon = pagePokemon[data];
    });
  },
});
</script>

<template>
  <div>
    <Navigation
      :side="pokemon.side"
      :image="pokemon.image"
      :background="pokemon.background"
    />
    <main tabindex="-1">
      <Nuxt />
    </main>
  </div>
</template>
