<template>
  <div class="content-desc-container">
    <content-info-item class="content-box-shadow content-panel" 
      v-for="(item, index) in info"
      :key="index"
      :src="item.src"
      :text="item.text"
    >
    </content-info-item>
  </div>
</template>

<script>
  import ContentInfoItem from './content-info-item'

  import superInfo from '../assets/img/info/super-tool-day.png'
  import locationInfo from '../assets/img/info/ic_location_b.png'
  import helpInfo from '../assets/img/info/ic_helpcenter.png'
  import universityInfo from '../assets/img/info/ic_platt-u.png'

  export default {
    name: 'content-info',
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
      'content-info-item': ContentInfoItem
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/content.scss';
</style>