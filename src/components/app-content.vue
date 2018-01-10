<template>
  <div class="app-content">
    <content-product-options> </content-product-options>
  </div>
</template>

<script>
  import ContentProductOptions from './content-product-options'

  export default {
    name: 'app-content',
    data: function () {
      return {}
    },
    components: {
      'content-product-options': ContentProductOptions
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
  @import '../assets/scss/colors.scss';

  .app-content {
    background-color: $light-grey;
    padding: 0 5px;
  }

</style>
