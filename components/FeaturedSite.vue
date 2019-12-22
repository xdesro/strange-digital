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
          <p class="featured-site-meta__date">9 December 2019</p>
        </div>
      </a>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.featured-container {
  grid-column-end: span 2;
  &__header {
    font-family: 'Orelo';
    font-style: italic;
    font-size: 3rem;
    text-transform: lowercase;
    text-align: right;
  }
}
.featured-site {
  &__link {
    color: inherit;
    text-decoration: none;
  }
  &__screenshot {
    margin-bottom: 0.875rem;
  }
}
.featured-site-meta {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-auto-flow: dense;
  align-items: end;
  align-content: center;
  justify-content: space-between;
  &__title {
    font-size: 1.5rem;
    font-weight: bold;
    color: $color__text;
    text-transform: uppercase;
  }
  &__url {
    grid-column: 1;
  }
  &__authorship {
    color: $color__text;
    text-align: right;
  }
  &__date {
    text-align: right;
  }
}
</style>
