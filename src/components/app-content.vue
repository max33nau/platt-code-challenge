<template>
  <div class="app-content">
    <content-product-options class="hide-not-mobile"> </content-product-options>
    <div class="text-center hide-not-mobile">
      <img class="content-box-shadow content-panel todays-deal-img" src="../assets/img/todays-deal.png" alt="Todays Deal"/>
    </div>
    <content-plus-member class="content-box-shadow content-panel"> </content-plus-member>
    <content-recently-viewed class="content-box-shadow content-panel"> </content-recently-viewed>
    <div class="content-info-container">
      <content-info class="content-box-shadow content-panel" 
        v-for="(item, index) in info"
        :key="index"
        :src="item.src"
        :text="item.text"
      >
      </content-info>
      <content-apps class="content-box-shadow content-panel"> </content-apps>  
    </div>
  </div>
</template>

<script>
  import ContentProductOptions from './content-product-options'
  import ContentPlusMember from './content-plus-member'
  import ContentRecentlyViewed from './content-recently-viewed'
  import ContentInfo from './content-info'
  import ContentApps from './content-apps'

  import superInfo from '../assets/img/info/super-tool-day.png'
  import locationInfo from '../assets/img/info/ic_location_b.png'
  import helpInfo from '../assets/img/info/ic_helpcenter.png'
  import universityInfo from '../assets/img/info/ic_platt-u.png'

  export default {
    name: 'app-content',
    data: function () {
      return {
        info: [
          {
            src: superInfo,
            text: 'Super Tool Day & Dynamic Data Day'
          },
          {
            src: locationInfo,
            text: 'Branch Locations'
          },
          {
            src: helpInfo,
            text: 'Help Center'
          },
          {
            src: universityInfo,
            text: 'Platt University'
          }
        ]
      }
    },
    components: {
      'content-product-options': ContentProductOptions,
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

  .content-info-container {
    display: flex;
    justify-content: space-between;
    width: 100%;
    flex-wrap: wrap;
  }

    @media screen and (min-width: $mobile-conatiner) {
      .app-content {
        padding: 0 15px;
      }
    } 


</style>
