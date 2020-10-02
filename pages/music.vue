<template>
  <div class="container">
    <div>
      <Header />
      <!-- start main header -->
      <section class="section header">
        <div class="wrapper-inner">
          <div class="content">
            <h1 class="page-heading">Music</h1>
            <p class="standfirst">
              A range of tracks from the back catalogue, remixes and some
              SoundCloud exclusives
            </p>
          </div>
        </div>
      </section>
      <!-- end main header -->

      <!-- start tabs -->
      <section class="section section-tabs tabs" role="main">
        <div class="wrapper-inner">
          <div class="tabs-nav" role="navigation">
            <ul class="tabs-nav-list" role="list">
              <li class="list-item active">
                <a href="#new">Recent</a>
              </li>
              <li class="list-item">
                <a href="#remixes">Remixes</a>
              </li>
              <li class="list-item">
                <a href="#archives">Archives</a>
              </li>
            </ul>
          </div>
          <div class="tabs-content active" id="new">
            <ul class="item-list" role="list">
              <li>No data</li>
            </ul>
          </div>
          <div class="tabs-content" id="remixes">
            <ul class="item-list" role="list">
              <li class="list-item">
                <h3 class="item-heading">Track4</h3>
              </li>
              <li class="list-item">
                <h3 class="item-heading">Track5</h3>
              </li>
              <li class="list-item">
                <h3 class="item-heading">Track6</h3>
              </li>
            </ul>
          </div>
          <div class="tabs-content" id="archives">
            <ul class="item-list" role="list">
              <li class="list-item">
                <h3 class="item-heading">Track7</h3>
              </li>
              <li class="list-item">
                <h3 class="item-heading">Track8</h3>
              </li>
              <li class="list-item">
                <h3 class="item-heading">Track9</h3>
              </li>
            </ul>
          </div>
        </div>
      </section>
      <!-- end tabs -->
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

.tabs-content {
  display: none;
}
.tabs-content.active {
  display: block;
}
</style>
