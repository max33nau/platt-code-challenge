<template>
  <div class="main-container">
    <app-header></app-header>
    <app-options></app-options>
  </div>
</template>

<script>
import AppHeader from './components/app-header.vue'
import AppOptions from './components/app-options.vue'

export default {
  name: 'app',
  components: {
    'app-header': AppHeader,
    'app-options': AppOptions
  }
}
</script>

<style lang="scss">
  @import './assets/scss/layout.scss';  
  @import './assets/scss/base.scss';
</style>
