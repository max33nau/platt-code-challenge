<template>
  <div class="app-content">
    <content-product-options> </content-product-options>
    <img class="content-box-shadow content-panel todays-deal-img" src="../assets/img/todays-deal.png" alt="Todays Deal"/>
    <content-plus-member class="content-box-shadow content-panel"> </content-plus-member>
    <content-recently-viewed class="content-box-shadow content-panel"> </content-recently-viewed>
  </div>
</template>

<script>
  import ContentProductOptions from './content-product-options'
  import ContentPlusMember from './content-plus-member'
  import ContentRecentlyViewed from './content-recently-viewed'

  export default {
    name: 'app-content',
    data: function () {
      return {}
    },
    components: {
      'content-product-options': ContentProductOptions,
      'content-plus-member': ContentPlusMember,
      'content-recently-viewed': ContentRecentlyViewed
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
  @import '../assets/scss/colors.scss';

  .app-content {
    background-color: $light-grey;
    padding: 0 7px;
  }

  $content-box-shadow: 0px 0px 5px 0px rgba(0,0,0,0.75);
  .content-box-shadow {
    -webkit-box-shadow: $content-box-shadow;
    -moz-box-shadow: $content-box-shadow;
    box-shadow: $content-box-shadow;
  }

  .content-panel {
    margin-bottom: 15px;
    background-color: $content-panel-bg;
  }

  .todays-deal-img {
    display: inline-block;
    max-width: 100%;
  }



</style>
