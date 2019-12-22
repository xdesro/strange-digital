<template>
  <div class="app">
    <!-- <header class="page-header">
      <div class="page-header__logo">
        <h1 class="page-header__title">
          <span class="page-header__title-hidden">Strange.Digital</span>
          <Logo />
        </h1>
        <p class="page-header__subtitle">Wondrous & peculiar websites.</p>
      </div>
    </header> -->
    <section class="landing-hero">
      <p class="landing-description">
        The latest and freshest sick af websites delivered hot-and-ready to your
        door or your email inbox via the newsletter. Lorem ipsum dolor sit amet,
        consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore
        et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
        exercitation ullamco laboris nisi ut aliquip
        <nuxt-link to="/about">sign up for the release letter</nuxt-link>.
      </p>
      <FeaturedSite />
    </section>
    <section class="gallery">
      <GallerySite />
      <GallerySite />
      <GallerySite />
      <GallerySite />
      <GallerySite />
    </section>
  </div>
</template>

<script>
import FeaturedSite from '~/components/FeaturedSite'
import GallerySite from '~/components/GallerySite'
export default {
  components: {
    FeaturedSite,
    GallerySite
  }
}
</script>

<style lang="scss">
.landing-hero {
  @include container;
  display: grid;
  grid-column-gap: 2.5rem;
  grid-template-columns: repeat(3, 1fr);
  align-items: end;
  margin-top: 4rem;
  margin-bottom: 2.5rem;
}
.landing-description {
  font-weight: 300;
  font-size: 0.75rem;
  color: $color__text;
  margin-bottom: 4.25rem;
}
.gallery {
  @include container;
  display: grid;
  grid-gap: 2.5rem;
  grid-template-columns: repeat(3, 1fr);
  margin-bottom: 5rem;
}
</style>
