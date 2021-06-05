<template>
  <div>
    <section class="hero is-large top-hero">
      <div class="hero-body">
        <div class="container">
          <div class="columns">
            <div class="column is-half">
              <p class="title">Muhammad Usman</p>
              <p class="intro">Software Engineer @ Cisco</p>
              <br>
              <button class="button is-primary is-light">
                <a href="mailto:me@usmanmuhd.com">
                  Get In Touch
                </a>
              </button>
            </div>
            <div class="column">
              <p class="intro">Site Under Construction</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style scoped>
.top-hero {
  background-color: var(--hero-bg-color);
}
.title {
  font-size: 400%;
}
.intro {
  font-size: 40px;
}
@media (max-width: 1023px) {
  .title {
    font-size: 300%;
  }
  .intro {
    font-size: 30px;
  }
}
</style>
