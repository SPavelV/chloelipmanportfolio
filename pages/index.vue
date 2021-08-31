<template>
  <div>
    <nuxt-link to="/">Home Page</nuxt-link>
    <nuxt-link to="/other">Other</nuxt-link>
    <div>
      <prismic-rich-text :field="page.titre_de_page" />
      <prismic-rich-text :field="page.contenu_test" />
      <prismic-image :field="page.image_test" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutPage',
  async asyncData({ $prismic, error }) {
    try {
      const pageContent = (await $prismic.api.getSingle('my_test_page')).data
      return {
        page: pageContent
      }
    } catch (e) {
      error({ statusCode: 404, message: 'Page not found' })
    }
  },
  data() {
    return {
      page: null
    }
  }
}
</script>
