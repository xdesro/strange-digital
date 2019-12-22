<template>
  <ul class="list-social">
    <li class="list-social__item" social="twitter">
      <a class="list-social__link" href="https://twitter.com/xdesro">
        Twitter
      </a>
    </li>
    <li class="list-social__item" social="github">
      <a
        class="list-social__link"
        href="https://github.com/xdesro/strange-digital"
      >
        GitHub
      </a>
    </li>
    <li class="list-social__item" social="email">
      <a class="list-social__link" href="mailto:yo@henry.codes">
        Electronic Mail
      </a>
    </li>
  </ul>
</template>
<style lang="scss">
.list-social {
  $social-svgs: ('github', 'twitter', 'email');
  font-size: 0.75rem;
  color: $color__text;
  &__link {
    color: inherit;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
  &__item {
    display: grid;
    grid-auto-flow: column;
    justify-content: start;
    grid-gap: 0.625rem;
    align-items: center;
    margin-bottom: 0.875rem;
    @each $social in $social-svgs {
      &[social='#{$social}'] {
        &:before {
          content: '';
          width: 1rem;
          height: 1rem;
          display: inline-block;
          background-image: url('../assets/icons/#{$social}.svg');
          background-size: contain;
          background-repeat: no-repeat;
          filter: $filter__icon;
        }
      }
    }
  }
}
</style>
