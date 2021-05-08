<template>
  <div>
    <!-- Navigation -->
    <nav class="navbar has-shadow is-fixed-top">
    <div class="bd-special-shadow"></div>
      <div class="container">
        <div class="navbar-brand">
          <nuxt-link to="/" class="navbar-item">
            <img src="../static/avatar.jpg" alt="Williamso">
          </nuxt-link>
          <button class="button navbar-burger" v-on:click="navToggle">
            <span></span>
            <span></span>
            <span></span>
          </button>
        </div>
        <div class="navbar-menu">
          <div class="navbar-start">
            <nuxt-link to="/" class="navbar-item">
              Awesome Williamso!
            </nuxt-link>
            <nuxt-link active-class="is-active" to="/" class="navbar-item is-tab" exact>Home</nuxt-link>
            <nuxt-link active-class="is-active" to="/about" class="navbar-item is-tab" exact>About</nuxt-link>
          </div>
          <div class="navbar-end">
            <a active-class="is-active" href="https://github.com/wizzy25" class="navbar-item is-tab" target ="_blank">
              <img src="../static/00_github.svg" alt="GitHub" />
            </a>
            <a href="https://www.xing.com/profile/Williams_Omayuku" class="navbar-item is-tab" target ="_blank" exact>
              <img src="../static/00_xing.svg" alt="Xing" />
            </a>
            <a href="https://www.linkedin.com/in/wizzy25/" class="navbar-item is-tab" target ="_blank" exact>
              <img src="../static/00_linkedin.svg" alt="LinkedIn" />
            </a>
            <a active-class="is-active" href="https://twitter.com/wizzy25_" class="navbar-item is-tab" target ="_blank" exact>
              <img src="../static/00_twitter.svg" alt="Twitter" />
            </a>
          </div>
        </div>
      </div>
    </nav>
    <!-- Navigation -->

    <!-- Display page contents -->
    <nuxt/>
  </div>
</template>

<script>
export default {
  methods: {
    navToggle () {
      const miniMenu = document.querySelector('.navbar-burger')
      // Get the target from the "data-target" attribute
      var menuItems = document.querySelector('.navbar-menu')
      // Toggle the class on both the "navbar-burger" and the "navbar-menu"
      miniMenu.classList.toggle('is-active')
      menuItems.classList.toggle('is-active')
    }
  }
}
</script>

