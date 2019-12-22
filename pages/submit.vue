<template>
  <main class="content content--submit">
    <h1>Submit</h1>
    <div>
      <p>
        So You’re Thinking About Submitting A Site? Awesome. We’d love to have
        you. Submissions are free, for the time being, so let’s see what you’ve
        got. We’re sure it’s beautiful and fantastic and everything we could
        ever dream of.
      </p>
      <p>
        We’ll use the power of the internet to get a screenshot of your site. We
        use Chrome via Puppetteer to screenshot, and the image will be captured
        at 1400x900px.
      </p>
      <p>
        Questions? Concerns? Reach out and touch faith (or like send us a DM or
        something).
      </p>
    </div>
    <FormSubmit />
  </main>
</template>

<script>
import FormSubmit from '~/components/FormSubmit'
export default {
  components: {
    FormSubmit
  }
}
</script>

<style></style>
