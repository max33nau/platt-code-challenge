<template>
  <div class="content-product-market">
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
    name: 'content-product-market',
    props: [ 'src', 'text' ]
  }
</script>

<style lang="scss" scoped>

  .content-product-market {
    display: inline-block;
    width: 15%;
    text-align: center;
    padding: 0px 0px 20px;
    min-height: 150px;
    position: relative;

    .image-container {
      img {
        min-height: 85px;
        width: 100%;
      }
    }

    .info-text {
      font-weight: bold;
      display: flex;
      min-height: 65px;
      align-items: center;
      justify-content: center;
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
    }
  }

</style>