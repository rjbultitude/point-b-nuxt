<template>
  <div class="container">
    <div>
      <Header />
      <!-- start main header -->
      <section class="section header">
        <div class="wrapper-inner">
          <div class="content">
            <h1 class="page-heading">Discography</h1>
            <p class="standfirst">
              How times have changed.<br />
              The graph below illustrates the evolution of formats across Point
              B's catalogue.<br />
              Click the squares to view release details
            </p>
          </div>
        </div>
      </section>
      <!-- end main header -->

      <!-- start content -->
      <section class="section section-infographic">
        <div class="wrapper-inner">
          <h2 class="heading-section">Discography infographic</h2>
          <div id="data-output">
            <p class="tooltip"></p>
          </div>
          <div class="sub-section sub-section-release-details">
            <figure class="figure release-figure">
              <img
                class="release-image"
                src="/images/discography/heart-of-matter"
                alt="Point B - Heart of matter"
              />
            </figure>
            <dl class="release-details-list">
              <dt class="visuallyhidden">Title:</dt>
              <dd class="release-title heading-dd"></dd>
              <dt class="">Label:</dt>
              <dd class="release-label"></dd>
              <dt class="">Cat No.:</dt>
              <dd class="release-cat"></dd>
              <dt class="">Format:</dt>
              <dd class="release-format"></dd>
              <dt class="">Year:</dt>
              <dd class="release-year"></dd>
            </dl>
          </div>
        </div>
      </section>
      <!-- end content -->
      <SocialSection />
    </div>
  </div>
</template>

<script>
export default {}
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
