<template>
  <nav class="top-nav">
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

<style lang="scss">
.top-nav {
  max-width: 16rem;
  &__list {
    list-style: none;
    margin: 0;
    padding: 0;
    display: grid;
    grid-auto-flow: column;
    text-transform: uppercase;
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
