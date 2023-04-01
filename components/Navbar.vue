<template>
  <div id="nav-wrapper">
    <nav class="main-nav">
      <div class="container full-height">
        <div class="nav-wrapper">
          <a href="#home" class="brand-logo">
            <img src="~/assets/images/alluvial.svg" alt="Alluvial" class="logo">
          </a>

          <ul id="nav-mobile-2" class="dn-mobile ul-nav">
            <li>
              <a href="#" data-target="slide-out" class="sidenav-trigger sec-color right">
                <img src="~/assets/images/menu.svg" alt="menu" class="">
              </a>
            </li>
          </ul>

          <ul id="nav-mobile" class="right hide-on-med-and-down">
            <li>
              <a href="#home">
                <span>Home</span>
              </a>
            </li>
            <li>
              <a href="#our-partners">
                <span>Our Partners</span>
              </a>
            </li>
            <li>
              <a href="#focus-crops">
                <span>Focus Crops</span>
              </a>
            </li>
            <li>
              <a href="#contact-us">
                <span>Contact Us</span>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <ul id="slide-out" class="sidenav">
      <div class="sidenav-logo">
        <a href="#home" class="sidenav-close">
          <img src="~/assets/images/alluvial.svg" alt="Alluvial" class="logo">
        </a>
      </div>
      <ul class="sidenav-flex">
        <li>
          <a href="#home" class="sidenav-close">
            <span>Home</span>
          </a>
        </li>
        <li>
          <a href="#our-partners" class="sidenav-close">
            <span>Our Partners</span>
          </a>
        </li>
        <li>
          <a href="#focus-crops" class="sidenav-close">
            <span>Focus Crops</span>
          </a>
        </li>
        <li>
          <a href="#contact-us" class="sidenav-close">
            <span>Contact Us</span>
          </a>
        </li>
      </ul>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'NavbarComp',
  mounted () {
    const M = require('materialize-css')

    const elemsSidenav = document.querySelectorAll('.sidenav')
    M.Sidenav.init(elemsSidenav)
    const elemsScrollspy = document.querySelectorAll('.scrollspy')
    M.ScrollSpy.init(elemsScrollspy)
  },
  methods: {
    scrollToTop () {
      window.scrollTo(0, 0)
    }
  }
}
</script>

<style scoped src="..\assets\css\navbar.css"></style>

<style scoped>
  .scrolled-nav .sidenav-trigger img {
    background-color: var(--pry-color);
    border-radius: 50%;
  }
</style>
