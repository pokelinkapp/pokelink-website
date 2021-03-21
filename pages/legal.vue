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
  head() {
    return {
      title: 'Pokélink | Legal',
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
    <main class="right">
      <h1 class="title">Legal</h1>
      <p>We don't collect any user-specific data about you as an individual.</p>
      <ul>
        <li>
          We use Google Analytics to know how popular each theme is, and to
          improve your experience (all we see is the URL among other generic
          web-metadata - we turned off what we could to minimize data collection
          on Google's part)
        </li>
        <li>
          We use a tool called sentry to anonymously submit any code-breaking
          bugs in the app to us so we can fix underlying issues.
        </li>
      </ul>
      <p>
        You can review our privacy policy here -
        http://pokelink.cybershade.org/privacy-policy.html
      </p>
      <p>
        By using the app - you agree to this. (Basically by using the app,
        general non-specific usage and bugs are collected and stored for ~60
        days to help us improve things.
      </p>
    </main>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: block;
}

h1 {
  font-size: 50px;
  font-weight: 900;
  margin-bottom: 40px;
  position: relative;

  &:before {
    content: '';
    display: block;
    height: 40px;
    width: 10px;
    position: absolute;
    left: -30px;
    top: 4px;
    background: #c47be6;
  }
}

p,
ul {
  margin-bottom: 40px;
  font-size: 20px;
  font-weight: 100;
}

li {
  margin-bottom: 20px;
  list-style: disc;
  margin-left: 20px;

  &:last-child {
    margin-bottom: 0;
  }
}
</style>
