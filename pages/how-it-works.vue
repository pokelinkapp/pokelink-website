<script lang="ts">
import Vue from 'vue';
import ghastly from '../assets/img/ghastly.jpg';
import Multiplayer from '../assets/icons/multiplayer.svg?inline';
import Support from '../assets/icons/support.svg?inline';
import Customise from '../assets/icons/customize.svg?inline';

export default Vue.extend({
  components: {
    Multiplayer,
    Support,
    Customise,
  },
  data() {
    return {
      nav: {
        side: 'right',
        image: ghastly,
        background: '#382A39',
      },
    };
  },
  head() {
    return {
      title: 'Pokélink | How it works',
    };
  },
  computed: {
    supportedVersions() {
      const list = [
        'Blue',
        'Red',
        'Yellow',
        'Leaf Green',
        'Fire Red',
        'Ruby',
        'Sapphire',
        'Emerald',
        'Diamond',
        'Pearl',
        'Platinum',
        'Heart Gold',
        'Soul Silver',
        'Black',
        'White',
        'Black 2',
        'White 2',
        'X',
        'Y',
        'Omega Ruby',
        'Alpha Sapphire',
        'Sun',
        'Moon',
        'Ultra Sun',
        'Ultra Moon',
      ].map((title) => `<span>${title}</span>`);

      const last = list.pop();

      return list.join(', ') + ' and ' + last;
    },
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
      <h1 class="sr-only">Features</h1>
      <ul>
        <li class="item">
          <Multiplayer />
          <div class="item__text">
            <h2>Multiplayer</h2>
            <p>
              The multiplayer support allows you to easily imports a partners
              Pokémon into your stream.
            </p>
          </div>
        </li>
        <li class="item">
          <Support style="width: 221px; height: 50px" />
          <div class="item__text">
            <h2>Support</h2>
            <p>
              Auto tracking is currently supporting Pokémon versions
              <span v-html="supportedVersions"></span>
              For all other versions, Manual tracking is available.
            </p>
          </div>
        </li>
        <li class="item">
          <Customise />
          <div class="item__text">
            <h2>Customise</h2>
            <p>
              Simple browser sources and easy to install custom themes for your
              stream; with plenty of default choices!
            </p>
          </div>
        </li>
      </ul>
    </main>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}

.item {
  display: flex;
  margin-bottom: 30px;

  svg {
    height: 50px;
    margin-right: 20px;
  }

  h2 {
    font-size: 50px;
    font-weight: 700;
    color: #e8536a;
    margin-bottom: 10px;
  }

  p {
    font-size: 20px;
    line-height: 24px;
    font-weight: 200;
    width: 50%;

    span {
      font-weight: 600;
    }
  }
}
</style>
