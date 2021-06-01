<template>
  <div class="container">
    <div>
      <div>
        <h1 v-if="error.statusCode === 404">Error 404 - Page not found</h1>
        <h1 v-else>An error occurred - {{ error.statusCode }} </h1>
      </div>
      <h2>Site under construction!</h2>
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
export default Vue.extend({
  props: ['error']
});
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
