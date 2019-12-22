<template>
  <nav class="top-nav">
    <nuxt-link class="top-nav__brand" to="/">strange.digital</nuxt-link>
    <ul class="top-nav__list">
      <li class="top-nav__list-item">
        <nuxt-link class="top-nav__link" to="/">Sites</nuxt-link>
      </li>
      <li class="top-nav__list-item">
        <nuxt-link class="top-nav__link" to="/about">About</nuxt-link>
      </li>
      <li class="top-nav__list-item">
        <nuxt-link class="top-nav__link" to="/submit">Submit</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  components: {}
}
</script>

<style lang="scss">
.top-nav {
  @include container;
  display: grid;
  // justify-items: end;
  justify-content: space-between;
  grid-auto-flow: column;
  padding-block: 2.5rem;
  &__brand {
    font-family: 'Orelo';
    font-size: 1.5rem;
    color: inherit;
    text-decoration: none;
  }
  &__list {
    list-style: none;
    margin: 0;
    padding: 0;
    display: inline-grid;
    grid-auto-flow: column;
    text-transform: uppercase;
    grid-column-gap: 2rem;
    justify-content: space-between;
    font-weight: 500;
    align-items: center;
  }
  &__link {
    color: inherit;

    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
}
</style>
