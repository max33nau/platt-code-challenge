<template>
  <div class="content-product-markets">
    <h3 class="text-center header"> Product Markets </h3>
    <div class="content-desc-container">
      <content-product-item class="content-box-shadow content-panel" 
        v-for="(item, index) in info"
        :key="index"
        :src="item.src"
        :text="item.text"
      >
      </content-product-item>
    </div>
  </div>
</template>

<script>
  import ContentProductItem from './content-product-item.vue'

  import dataCommImg from '../assets/img/product-markets/datacomm.png'
  import hvacImg from '../assets/img/product-markets/hvac.png'
  import industrialImg from '../assets/img/product-markets/industrial.png'
  import lightingImg from '../assets/img/product-markets/lighting.png'
  import engeryImg from '../assets/img/product-markets/energy.png'
  import utilityImg from '../assets/img/product-markets/utility.png'

  export default {
    name: 'content-product-markets',
    data: function () {
      return {
        info: [
          {
            src: dataCommImg,
            text: 'DataComm'
          },
          {
            src: hvacImg,
            text: 'HVAC'
          },
          {
            src: industrialImg,
            text: 'Industrial'
          },
          {
            src: lightingImg,
            text: 'Lighting'
          },
          {
            src: engeryImg,
            text: 'Energy Efficiency'
          },
          {
            src: utilityImg,
            text: 'Utility'
          }
        ]
      }
    },
    components: {
      'content-product-item': ContentProductItem
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/colors.scss';
  @import '../assets/scss/content.scss';

  .content-product-markets {
    margin-bottom: 10px;

    .header {
      margin: 0;
      padding: 20px 0;
    }
  }


</style>