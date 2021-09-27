<template>
  <div>
    <MainMenu />
    <!--<div>
      <prismic-rich-text :field="page.titre_de_page" />
      <prismic-rich-text :field="page.contenu_test" />
      <prismic-image :field="page.image_test" />
    </div>-->
  </div>
</template>

<script>
import MainMenu from '@/components/MainMenu'

export default {
  components: { MainMenu },

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

<style lang="css" src="~/assets/css/main.css"></style>
