<template>
  <div class="section section-main-header" role="banner">
    <div class="logo">Point.B</div>
    <nav id="main-nav" role="navigation" class="nav nav-main">
      <a href="main-nav" class="btn-nav">
        <span class="text">Open navigation</span>
        <span class="icon">
          <svg
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            x="0px"
            y="0px"
            viewBox="0 0 748.9 436.8"
            enable-background="new 0 0 748.9 436.8"
            xml:space="preserve"
          >
            <path
              d="M703.9,89.9H43.7C19.3,89.9,0,69.4,0,45S19.3,0,43.7,0h661.5c24.4,0,43.7,20.6,43.7,45S728.3,89.9,703.9,89.9z"
            />
            <path
              d="M703.9,269.8H43.7c-24.4,0-43.7-20.6-43.7-45s19.3-45,43.7-45h661.5c24.4,0,43.7,20.6,43.7,45S728.3,269.8,703.9,269.8z"
            />
            <path
              d="M703.9,436.8H43.7c-24.4,0-43.7-20.6-43.7-45s19.3-45,43.7-45h661.5c24.4,0,43.7,20.6,43.7,45
  C748.9,416.3,728.3,436.8,703.9,436.8z"
            />
          </svg>
        </span>
      </a>
      <ul role="list" class="nav-list nav-main-list">
        <li class="list-item">
          <NuxtLink to="/">Home page</NuxtLink>
          <!-- <a class="nav-link" href="/" id="home-link">Home</a> -->
        </li>
        <li class="list-item">
          <NuxtLink to="/music">Music</NuxtLink>
          <!-- <a class="nav-link" href="/music/index.html" id="music-link">Music</a> -->
        </li>
        <li class="list-item">
          <NuxtLink to="/discog">Discography</NuxtLink>
          <!-- <a class="nav-link" href="/discog/index.html" id="discog-link">
            Discog
          </a> -->
        </li>
        <!-- <li class="list-item">
          <a class="nav-link" href="patches.php" id="patches-link">Patches</a>
        </li> -->
      </ul>
    </nav>
  </div>
</template>

<style>
.header {
  border: 0 none;
}

#home .header .page-heading {
  margin-bottom: 0;
}

.section-main-header .wrapper-inner {
  position: relative;
}

.section-main-header .logo {
  color: white;
  font-size: 3.2em;
  line-height: 1.8em;
  text-align: left;
}
</style>
