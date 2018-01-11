<template>
  <div class="main-container">
    <app-header></app-header>
    <app-options></app-options>
    <app-content></app-content>
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from './components/app-header'
import AppOptions from './components/app-options'
import AppContent from './components/app-content'
import AppFooter from './components/app-footer'

export default {
  name: 'app',
  components: {
    'app-header': AppHeader,
    'app-options': AppOptions,
    'app-content': AppContent,
    'app-footer': AppFooter
  }
}
</script>

<style lang="scss">
  @import './assets/scss/layout.scss';  
  @import './assets/scss/base.scss';
</style>
