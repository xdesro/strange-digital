<template>
  <div>
    <nuxt />
  </div>
</template>

<style lang="scss">
@import url('https://rsms.me/inter/inter.css');
html {
  font-family: 'Inter', sans-serif;
}
@supports (font-variation-settings: normal) {
  html {
    font-family: 'Inter var', sans-serif;
  }
}
body {
  background-color: $light-theme--background;
  color: $accent--primary;
}
img {
  max-width: 100%;
  display: block;
}
</style>
