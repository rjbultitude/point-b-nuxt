<template>
  <div class="container">
    <div>
      <h1 class="title">point-b</h1>
      <h1 v-html="content.index.title"></h1>
      <div v-html="content.index.content"></div>
      <SocialSection />
      <Releases :releases="releases.releases" test="testData" />
    </div>
  </div>
</template>

<script>
import contentConfig from '../content.config'
import releasesConfig from '../releases.config'
export default {
  head() {
    return { title: this.content.title }
  },
  async asyncData({ $content }) {
    const content = await $content(contentConfig.CONTENT).fetch()
    const releases = await $content(releasesConfig.CONTENT).fetch()
    return { content, releases }
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
