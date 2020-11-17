<template>
  <div class="wrapper">
    <Header />
    <Nuxt />
  </div>
</template>

<script>
import Header from '../components/Header'
export default {
  components: {
    Header,
  },
}
</script>

<style>
@import url(http://fonts.googleapis.com/css?family=Bitter:400,700);
@import url(http://fonts.googleapis.com/css?family=Roboto+Slab:300,100);

html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 1em;
  line-height: 1;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

body {
  background-color: #f9b766;
}

.figure img {
  width: 100%;
}

.image-border {
  padding: 8px;
  background-color: rgba(255, 255, 255, 0.8);
}
</style>
