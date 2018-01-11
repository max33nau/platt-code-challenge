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

  .content-info-item {
    display: inline-block;
    width: 48%;
    text-align: center;
    padding: 20px 15px;
    min-height: 175px;
    position: relative;

    .info-text {
      font-weight: bold;
      display: flex;
      min-height: 45px;
      align-items: center;
      justify-content: center;
      position: absolute;
      left: 0;
      right: 0;
      bottom: 10px;
    }
  }

</style>