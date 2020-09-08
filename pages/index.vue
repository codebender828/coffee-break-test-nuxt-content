<template>
  <c-box as="article" py="20" :max-w="['95%', '90%', 'md']" mx="auto">
    <h1 v-chakra mb="5" font-weight="bold" font-size="3xl">
      {{ page.title }}
    </h1>
    <nuxt-content :document="page" />
  </c-box>
</template>

<script>
export default {
  async asyncData ({ $content }) {
    const page = await $content('hello').fetch()

    return {
      page
    }
  }
}
</script>

<style>
/* Nuxt content element styles go here */
.nuxt-content p {
  /* my custom h1 style */
  margin-bottom: 1rem;
  margin-top: 0.75rem
}

.nuxt-content h2 {
  /* my custom h1 style */
  font-size: 1.3em;
  font-weight: bold
}
</style>
