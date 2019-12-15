<template>
  <div class="featured-container">
    <h2 class="featured-container__header">Site of the day</h2>
    <div class="featured-site">
      <a href="#" class="featured-site__link">
        <img
          src="~/assets/img/screenshot-canals.png"
          class="featured-site__screenshot"
        />
        <div class="featured-site-meta">
          <p class="featured-site-meta__title">Canals Amsterdam</p>
          <p class="featured-site-meta__url">canals-amsterdam.nl</p>
          <p class="featured-site-meta__authorship">
            Aristide Benoist & Marcus Brown
          </p>
          <p class="featured-site-meta__data">9 December 2019</p>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.featured-site {
  &__screenshot {
    max-width: 40rem;
  }
}
</style>
