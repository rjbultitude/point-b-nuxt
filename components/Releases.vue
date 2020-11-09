<template>
  <div class="section">
    <h2 class="logo">Releases</h2>
    <article>
      <nuxt-content :document="article" />
    </article>
  </div>
</template>

<script>
// import dataConf from '../data-conf'

export default {
  async asyncData({ $content }) {
    const article = await $content('articles').fetch()
    return { article }
  },
}
</script>
