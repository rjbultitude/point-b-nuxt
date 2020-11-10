<template>
  <div class="section">
    <h2 class="logo">Releases</h2>
    <article>
      <!-- {{ $log('test: ', test) }} -->
      <h1 v-html="releases.r001.title"></h1>
      <div v-html="releases.r001.year"></div>
    </article>
  </div>
</template>

<script>
export default {
  props: {
    releases: {
      type: Object,
      required: true,
    },
    test: {
      type: String,
      default: '',
    },
  },
}
</script>
