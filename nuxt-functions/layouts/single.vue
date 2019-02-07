<template>
  <div>
    <span>single layout</span>
    <SinglePage />
    <hr>

    <nuxt />

    <hr>
    <footer>
      footer
    </footer>
  </div>
</template>

<script>
import SinglePage from '~/components/AppNavigation.vue'

export default {
  components: {
    SinglePage
  }
}
</script>
