<template>
  <div class="root">
    <TopNav />
    <nuxt />
    <PageFooter />
  </div>
</template>

<script>
import TopNav from '~/components/TopNav'
import PageFooter from '~/components/PageFooter'
export default {
  components: {
    TopNav,
    PageFooter
  }
}
</script>
<style lang="scss"></style>
