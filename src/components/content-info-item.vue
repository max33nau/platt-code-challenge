<template>
  <div class="content-info-item">
    <div class="image-container">
      <img
        :src="src"
      />
    </div>
    <div class="info-text">
      {{text}}
    </div>
  </div>
</template>

<script>
  export default {
    name: 'content-info-item',
    props: [ 'src', 'text' ]
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';

  .content-info-item {
    display: inline-block;
    width: 48%;
    text-align: center;
    padding: 20px 15px;
    min-height: 175px;
    position: relative;

    .info-text {
      font-weight: bold;
      display: -webkit-box; /* OLD - iOS 6-, Safari 3.1-6 */
      display: -moz-box;    /* OLD - Firefox 19- */
      display: -ms-flexbox;  /*  IE 10 */
      display: -webkit-flex; /* NEW - Chrome */
      display: flex;
      min-height: 45px;
      -webkit-align-items: center;
      align-items: center;
      -webkit-box-pack: center;
      -moz-box-pack: center;
      -ms-flex-pack: center;
      -webkit-justify-content: center;
      justify-content: center;
      position: absolute;
      left: 0;
      right: 0;
      bottom: 10px;
    }
  }

  @media screen and (min-width: $mobile-conatiner) {
    .content-info-item {
      width: 21%;
      min-height: 180px;
    }
  } 

</style>