<template>
  <div class="container">
    <section class="section header">
      <div class="wrapper-inner">
        <h1 class="title">Point B</h1>
        <h3 v-html="content.index.title"></h3>
        <div v-html="content.index.content"></div>
        <div class="content">
          <h2 class="page__heading">
            Music, sound design
            <span class="special-character">&amp;</span>
            software
          </h2>
        </div>
      </div>
    </section>
    <!-- start homepage news -->
    <article class="article article-news">
      <div class="wrapper-inner">
        <h2 class="article__heading">
          <span class="lesser">Latest EP </span>
          Smash Hits
          <span class="lesser">Out Now</span>
        </h2>
        <div class="article__text">
          <p>Four heavyweight slabs of techno</p>
          <p class="aux-info">Available on 12" Vinyl/Digital</p>
        </div>
        <div class="article__figure">
          <div class="image-border">
            <img src="/images/discography/Smash-Hits.jpg" alt="Smash Hits EP" />
          </div>
        </div>
        <aside class="aside buy-links">
          <a
            href="https://www.juno.co.uk/search/?q%5Ball%5D%5B0%5D=point+b+smash+hits&hide_forthcoming=0&media_type=vinyl"
            target="_blank"
            class="btn-cta"
          >
            <span class="icon">
              <svg
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                x="0px"
                y="0px"
                viewBox="0 0 63 62.8"
                enable-background="new 0 0 63 62.8"
                xml:space="preserve"
              >
                <circle fill="#FFFFFF" cx="31.5" cy="31.5" r="31.5" />
                <g>
                  <polyline
                    fill="none"
                    stroke="#C74F3E"
                    stroke-width="4"
                    stroke-miterlimit="10"
                    points="51.2,17 43,36.4 20.1,36.4 13.2,24.4 37,24.4"
                  />
                  <circle fill="#C74F3E" cx="19.7" cy="46.4" r="4.7" />
                  <circle fill="#C74F3E" cx="41.7" cy="46.4" r="4.7" />
                </g>
              </svg>
            </span>
            <span class="text">Buy 12" Vinyl</span>
          </a>
          <a
            href="https://boomkat.com/products/smash-hits"
            target="_blank"
            class="btn-cta"
          >
            <span class="icon">
              <svg
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                x="0px"
                y="0px"
                viewBox="0 0 63 62.8"
                enable-background="new 0 0 63 62.8"
                xml:space="preserve"
              >
                <circle fill="#FFFFFF" cx="31.5" cy="31.5" r="31.5" />
                <g>
                  <polyline
                    fill="none"
                    stroke="#C74F3E"
                    stroke-width="4"
                    stroke-miterlimit="10"
                    points="51.2,17 43,36.4 20.1,36.4 13.2,24.4 37,24.4"
                  />
                  <circle fill="#C74F3E" cx="19.7" cy="46.4" r="4.7" />
                  <circle fill="#C74F3E" cx="41.7" cy="46.4" r="4.7" />
                </g>
              </svg>
            </span>
            <span class="text">Buy digital</span>
          </a>
          <a
            href="https://open.spotify.com/album/4o4bD5oktxEFjEunf9Js8T?si=V8O1_xj1Rg69YQ1YrkuvoA"
            target="_blank"
            class="btn-cta"
          >
            <span class="icon">
              <svg
                version="1.1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                x="0px"
                y="0px"
                viewBox="0 0 62.8 63"
                enable-background="new 0 0 62.8 63"
                xml:space="preserve"
              >
                <circle fill="#FFFFFF" cx="31.3" cy="31.5" r="31.5" />
                <g>
                  <path
                    fill="none"
                    stroke="#C74F3E"
                    stroke-width="4"
                    stroke-miterlimit="10"
                    d="M12.2,28.9c0-10.5,8.5-19,19-19s19,8.5,19,19"
                  />
                  <path
                    fill="#C74F3E"
                    d="M12.2,43.8L12.2,43.8c-1.9,0-3.4-1.5-3.4-3.4v-6.2c0-1.9,1.5-3.4,3.4-3.4h0c1.9,0,3.4,1.5,3.4,3.4v6.2
                      C15.5,42.2,14,43.8,12.2,43.8z"
                  />
                  <path
                    fill="#C74F3E"
                    d="M50.1,43.8L50.1,43.8c-1.9,0-3.4-1.5-3.4-3.4v-6.2c0-1.9,1.5-3.4,3.4-3.4h0c1.9,0,3.4,1.5,3.4,3.4v6.2
                      C53.5,42.2,52,43.8,50.1,43.8z"
                  />
                </g>
              </svg>
            </span>
            <span class="text">Play on Spotify</span>
          </a>
        </aside>
      </div>
    </article>
    <!-- end homepage news -->
    <SocialSection />
    <Releases :releases="releases.releases" test="testData" />
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
  text-align: center;
}

.title {
  display: block;
  font-weight: 300;
  font-size: 1.8rem;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 1.3rem;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.wrapper-inner {
  max-width: 960px;
  margin: 0 auto;
}

.page__heading {
  color: white;
  font-size: 4rem;
  font-family: 'bitter', 'Gill Sans', 'Helvetica Neue', Arial, sans-serif;
  mask-image: url(/images/decoration/knockout.png);
}

.header {
  background-color: rgba(5, 57, 94, 0.8);
}

.links {
  padding-top: 15px;
}

.article .wrapper-inner {
  display: flex;
  flex-direction: column;
}

.article__heading {
  flex-basis: 100%;
}

.article__text,
.article__figure,
.article .buy-links {
  flex-basis: 100%;
}

.article__figure img {
  width: 100%;
}

.article .buy-links {
  display: flex;
  flex-direction: row;
}

.buy-links .btn-cta {
  flex-basis: 33.2%;
}

@media screen and (min-width: 700px) {
  .article .wrapper-inner {
    flex-direction: row;
  }

  .article__text {
    flex-basis: 20%;
  }

  .article .figure {
    flex-basis: 60%;
  }

  .article .buy-links {
    flex-basis: 20%;
    flex-direction: column;
  }

  .buy-links .btn-cta {
    flex-basis: 100%;
  }
}
</style>
