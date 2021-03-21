<script>
import image from '../assets/img/jolteon.jpg';
import Twitter from '../assets/icons/twitter.svg?inline';
import Facebook from '../assets/icons/fb.svg?inline';
import Discord from '../assets/icons/discord.svg?inline';
export default {
  name: 'Navigation',
  components: {
    Twitter,
    Facebook,
    Discord,
  },
  props: {
    side: {
      type: String,
      default: 'right',
    },
    image: {
      type: String,
      default: image,
    },
    background: {
      type: String,
      default: '#FFDE53',
    },
  },
};
</script>

<template>
  <div class="navigation">
    <nav>
      <ul class="navigation__menu">
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">About us</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/how-it-works">How it works</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/legal">Legal</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/contact">Contact us</NuxtLink>
        </li>
      </ul>
    </nav>
    <nav>
      <ul class="navigation__social">
        <li>
          <a
            href="https://twitter.com/PokelinkApp"
            target="_blank"
            rel="noopener noreferrer"
            title="Twitter"
            ><Twitter
          /></a>
        </li>
        <li>
          <a href="" target="_blank" rel="noopener noreferrer" title="Facebook"
            ><Facebook
          /></a>
        </li>
        <li>
          <a
            href="https://discord.pokelink.xyz"
            target="_blank"
            rel="noopener noreferrer"
            title="Discord"
            ><Discord
          /></a>
        </li>
      </ul>
    </nav>
    <div
      :class="{
        'navigation__pkmn-wrapper': true,
        'navigation__pkmn-wrapper--left': side === 'left',
        'navigation__pkmn-wrapper--right': side !== 'left',
      }"
      :style="{ background: background }"
    >
      <div class="navigation__pkmn" :style="{ background: background }">
        <img :src="image" alt="" class="navigation__pkmn-img" />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.navigation {
  &__menu {
    height: 100vh;
    position: fixed;
    left: 0;
    top: 0;
    display: flex;
    justify-content: center;
    flex-direction: column;
    width: 25vw;
    padding: 100px;
    padding-right: 0;
    z-index: 1;

    a {
      font-size: 20px;
      color: #242426;
      line-height: 24px;
      font-weight: 900;
      text-decoration: none;
      text-transform: uppercase;
      margin-bottom: 20px;
      display: block;
      position: relative;

      &.nuxt-link-exact-active:before {
        content: '';
        display: block;
        width: 20px;
        height: 20px;
        background: #242426;
        position: absolute;
        left: -40px;
        top: 2px;
      }

      &:hover {
        text-decoration: underline;
      }
    }
  }

  &__pkmn-wrapper {
    height: 100vh;
    width: 25vw;
    position: fixed;
    top: 0;

    &--left {
      left: 0;

      .navigation__pkmn {
        right: -100%;
        align-items: flex-end;
      }
    }

    &--right {
      right: 0;

      .navigation__pkmn {
        left: -100%;
        align-items: flex-start;
      }
    }
  }

  &__social {
    position: fixed;
    bottom: 0;
    left: 0;
    padding: 100px;
    display: flex;
    z-index: 1;

    a {
      margin-right: 20px;
    }

    a svg {
      width: 24px;
    }
  }

  &__pkmn {
    height: 150vh;
    width: 150vh;
    border-radius: 100%;
    overflow: hidden;
    transform: translateY(-15%);

    display: flex;

    justify-content: center;
    flex-direction: column;
    position: absolute;

    &-img {
      margin-left: 10%;
    }
  }
}
</style>
