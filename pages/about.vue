<template>
  <main class="content content--centered">
    <h1>About</h1>
    <p>
      Websites are sick and <span class="accent-text">strange.digital</span> is
      about sharing some of the most adventurous ones. We feature sites with a
      focus on experiential web, delightful interaction, technological
      innovation, and above all, a respect for the web platform.
    </p>
    <p>
      This website was created by Henry Desroches (<span class="accent-text"
        >xdesro</span
      >). It’s open-source, is built on Nuxt.js, and is served by Netlify. Check
      out the source code on GitHub, or get at us on Twitter.
    </p>
    <ListSocial />
  </main>
</template>

<script>
import ListSocial from '~/components/ListSocial'
export default {
  components: {
    ListSocial
  }
}
</script>

<style></style>
