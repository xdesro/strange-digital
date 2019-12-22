<template>
  <footer @click="toggleTheme" class="footer">
    <p class="footer__text">
      Soon you will have only a memory of this moment — © {{ year }} AD
    </p>
  </footer>
</template>

<script>
export default {
  computed: {
    year() {
      return new Date().getFullYear()
    }
  },
  methods: {
    toggleTheme() {
      document.documentElement.toggleAttribute('dark')
    }
  }
}
</script>

<style lang="scss">
.footer {
  cursor: pointer;
  position: fixed;
  transform: rotate(90deg);
  font-size: 0.75rem;
  font-weight: 500;
  text-transform: uppercase;
  transform-origin: bottom right;
  bottom: 3.75rem;
  right: 3.75rem;
}
</style>
