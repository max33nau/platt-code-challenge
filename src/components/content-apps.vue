<template>
  <div class="content-apps">
    <div class="app-image">
    </div>
    <h5 class="apps-text">
      Shop better, download the Platt App today
    </h5>
  </div>
</template>

<script>
  export default {
    name: 'content-apps'
  }
</script>

<style lang="scss" scoped>

  .content-apps {
    width: 100%;
    overflow: hidden;

    .app-image {
      min-height: 130px;
      background-image: url('../assets/img/app-get-banner.png');
      background-repeat: no-repeat;
      background-size: cover;
      background-position: right;

      @media screen and (max-width: 320px) {
        width: 108%;
      }
    }

    .apps-text {
      font-weight: bold;
      font-size: 16px;
      margin: 10px 0;
      padding: 0 10px;
      text-align: center;
    }

 
  }

</style>