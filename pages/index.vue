<template>
  <div class="app">
    <header class="page-header">
      <div class="page-header__logo">
        <h1 class="page-header__title">
          <span class="page-header__title-hidden">Strange.Digital</span>
          <Logo />
        </h1>
        <p class="page-header__subtitle">Wondrous & peculiar websites.</p>
      </div>
      <TopNav />
    </header>
    <p class="landing-description">
      The latest and freshest sick af websites delivered hot-and-ready to your
      door or your email inbox via the newsletter. Lorem ipsum dolor sit amet,
      consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et
      dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
      ullamco laboris nisi ut aliquip
      <nuxt-link to="/about">sign up for the release letter</nuxt-link>.
    </p>
    <FeaturedSite />
    <section class="gallery">
      <GallerySite />
    </section>
  </div>
</template>

<script>
import Logo from '~/components/Logo'
import TopNav from '~/components/TopNav'
import FeaturedSite from '~/components/FeaturedSite'
import GallerySite from '~/components/GallerySite'
export default {
  components: {
    Logo,
    TopNav,
    FeaturedSite,
    GallerySite
  }
}
</script>

<style lang="scss">
.page-header {
  display: grid;
  margin-top: 3rem;
  grid-auto-flow: column;
  &__logo {
    position: relative;
    max-width: 28.75rem;
  }
  &__title {
    &-hidden {
      position: absolute;
      visibility: hidden;
    }
  }

  &__subtitle {
    font-weight: 500;
    text-transform: uppercase;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    margin: 0 auto;
    text-align: center;
    font-size: 0.875rem;
  }
}
</style>
