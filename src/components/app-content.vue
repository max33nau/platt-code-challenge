<template>
  <div class="app-content">
    <content-product-options class="hide-not-mobile"> </content-product-options>
    <div class="text-center hide-not-mobile">
      <img class="content-box-shadow content-panel todays-deal-img" src="../assets/img/todays-deal.png" alt="Todays Deal"/>
    </div>
    <content-product-markets class="hide-on-mobile"> </content-product-markets>
    <content-plus-member class="content-box-shadow content-panel"> </content-plus-member>
    <div class="content-recent-container">
      <img class="content-box-shadow content-panel todays-deal-img hide-on-mobile" src="../assets/img/todays-deal.png" alt="Todays Deal"/>
      <content-recently-viewed class="content-box-shadow content-panel recent-viewed-container"> </content-recently-viewed>
    </div>
    <content-info> </content-info>
    <content-apps class="content-box-shadow content-panel"> </content-apps>  
  </div>
</template>

<script>
  import ContentProductOptions from './content-product-options'
  import ContentProductMarkets from './content-product-markets'
  import ContentPlusMember from './content-plus-member'
  import ContentRecentlyViewed from './content-recently-viewed'
  import ContentInfo from './content-info'
  import ContentApps from './content-apps'

  export default {
    name: 'app-content',
    components: {
      'content-product-options': ContentProductOptions,
      'content-product-markets': ContentProductMarkets,
      'content-plus-member': ContentPlusMember,
      'content-recently-viewed': ContentRecentlyViewed,
      'content-info': ContentInfo,
      'content-apps': ContentApps
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
  @import '../assets/scss/colors.scss';
  @import '../assets/scss/content.scss';

  .app-content {
    background-color: $light-grey;
    padding: 0 7px 5px;
    height: 100%;
  }

  .todays-deal-img {
    display: inline-block;
    max-width: 100%;
  }

  @media screen and (min-width: $mobile-conatiner) {
    .app-content {
      padding: 0 15px 5px;
    }

    .content-recent-container {
      display: flex;
      justify-content: space-between;

      $width-content: 49%;

      img {
        width: $width-content;
      }

      .recent-viewed-container {
        width: $width-content;
      }
    }
  } 

</style>
