<template>
  <div>
    <nav
      class="navbar is-fixed-top top-navbar"
      role="navigation"
      aria-label="main navigation"
    >
      <div class="container">
        <div class="navbar-brand">
          <a class="navbar-item" href="/">
            <div class="navbar-title">Muhammad Usman</div>
          </a>

          <a
            :aria-expanded="isActive"
            :class="{ 'is-active': isActive }"
            role="button"
            class="navbar-burger"
            aria-label="menu"
            data-target="navbarMenu"
            @click="isActive = !isActive"
          >
            <span aria-hidden="true" />
            <span aria-hidden="true" />
            <span aria-hidden="true" />
          </a>
        </div>

        <div
          :class="{ 'is-active': isActive }"
          id="navbarMenu"
          class="navbar-menu"
        >
          <div class="navbar-end">
            <a class="navbar-item" href="/about/"> About Me </a>
            <a class="navbar-item" href="/contact/"> Contact Me </a>
            <a class="navbar-item" href="/resume.pdf"> Resume </a>
          </div>
        </div>
      </div>
    </nav>
    <section class="hero">
      <div class="hero-body hidden-hero"></div>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      isActive: false,
      showNavbar: true,
    }
  },
})
</script>

<style scoped>
@media (min-width: 1024px) {
  .top-navbar {
    padding: 16px 0;
  }
  .hidden-hero {
    padding: 42.5px 0;
  }
}
@media (max-width: 1023px) {
  .hidden-hero {
    padding: 26.5px 0;
  }
}
.top-navbar {
  border-bottom: 1px solid var(--hero-bg-color);
}
.navbar.is-fixed-top {
  left: 0;
  position: fixed;
  right: 0;
  z-index: 30;
}
.navbar-title {
  font-weight: bold;
  font-size: var(--nav-title-font-size);
}
</style>
