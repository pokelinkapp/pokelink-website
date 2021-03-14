<script>
import image from '../assets/img/jolteon.jpg';
export default {
  name: 'Navigation',
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
  mounted() {
    console.log(this.image);
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

    a {
      font-size: 20px;
      color: black;
      line-height: 24px;
      font-weight: 900;
      text-decoration: none;
      text-transform: uppercase;

      &:hover {
        text-decoration: underline;
      }
    }
  }

  &__pkmn-wrapper {
    height: 100vh;
    width: 50vh;
    position: fixed;
    top: 0;

    &--left {
      left: 0;

      .navigation__pkmn {
        right: -100%;
        align-items: flex-end;
      }

      .navigation__pkmn-img {
        margin-right: 10%;
      }
    }

    &--right {
      right: 0;

      .navigation__pkmn {
        left: -100%;
        align-items: flex-start;
      }

      .navigation__pkmn-img {
        margin-left: 10%;
      }
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
  }
}
</style>
