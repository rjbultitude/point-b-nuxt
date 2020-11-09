<template>
  <div class="section">
    <h2 class="logo">Releases</h2>
    <!-- <nuxt-content :document="doc" /> -->
    <ul>
      <li>{content[0]title}</li>
    </ul>
  </div>
</template>

<script>
import dataConf from '../data-conf'

export default {
  head() {
    return { title: this.content.title }
  },
  async asyncData({ $content }) {
    const content = await $content(dataConf.CONTENT).fetch()
    return { content }
  },
}
</script>
