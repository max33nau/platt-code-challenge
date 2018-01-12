<template>
  <div class="content-recently-viewed">
    <h4 class="recent-view-header" >Recently viewed <span class="view-all"> View all </span> </h4>
    <div class="recently-viewed-images">
      <div class="recently-viewed-image-container" 
        v-for="(recent, index) in recentlyViewed"
        :key="index"
      >
        <img 
          :src="recent.src"
          :alt="recent.alt"
        />
      </div>
    </div>
  </div>
</template>

<script>
  import electricBox from '../assets/img/recently-viewed/11.png'
  import metalCapsule from '../assets/img/recently-viewed/22.png'

  export default {
    name: 'content-recently-viewed',
    data: function () {
      return {
        recentlyViewed: [
          {
            src: electricBox,
            alt: 'Electric Box'
          },
          {
            src: metalCapsule,
            alt: 'Metal capsule'
          },
          {
            src: metalCapsule,
            alt: 'Metal capsule'
          }
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/colors.scss';

  .content-recently-viewed {
    padding: 10px 15px;

    .recent-view-header {
      font-size: 14px;
      font-weight: bold;
      margin-top: 5px;
    }

    .recently-viewed-images {
      display: -webkit-box; /* OLD - iOS 6-, Safari 3.1-6 */
      display: -moz-box;    /* OLD - Firefox 19- */
      display: -ms-flexbox;  /*  IE 10 */
      display: -webkit-flex; /* NEW - Chrome */
      display: flex;
      -webkit-box-pack: space-between;
      -moz-box-pack: space-between;
      -ms-flex-pack: space-between;
      -webkit-justify-content: space-between;
      justify-content: space-between;
      margin-bottom: 5px;
    }

    .recently-viewed-image-container {
      display: inline-block;
      text-align: center;
      width: 30%;
    }

    img {
      max-width: 100%;
    }
  }

  .view-all {
    float: right;
    color: $content-panel-highlight-txt;
  }
</style>