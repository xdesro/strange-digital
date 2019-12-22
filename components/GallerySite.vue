<template>
  <div class="gallery-site">
    <a href="#" class="gallery-site__link">
      <img
        src="~assets/img/screenshot-schick-toikka.png"
        class="gallery-site__screenshot"
      />
      <div class="gallery-site-meta">
        <p class="gallery-site-meta__title">{{ site.name }}</p>
        <p class="gallery-site-meta__link">{{ site.url }}</p>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    site: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style lang="scss">
.gallery-site {
  &__link {
    text-decoration: none;
  }
  &__screenshot {
    margin-bottom: 0.625rem;
  }
}
.gallery-site-meta {
  &__title {
    font-size: 0.75rem;
    font-weight: 600;
    color: $color__text;
    text-transform: uppercase;
  }
  &__link {
    font-size: 0.625rem;
  }
}
</style>
