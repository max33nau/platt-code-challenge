<template>
  <div class="main-container">
    <app-header></app-header>
    <app-options></app-options>
    <app-content></app-content>
  </div>
</template>

<script>
import AppHeader from './components/app-header.vue'
import AppOptions from './components/app-options.vue'
import AppContent from './components/app-content.vue'

export default {
  name: 'app',
  components: {
    'app-header': AppHeader,
    'app-options': AppOptions,
    'app-content': AppContent
  }
}
</script>

<style lang="scss">
  @import './assets/scss/layout.scss';  
  @import './assets/scss/base.scss';
</style>
