<template>
  <div class="content-plus-member">
    <img src="../assets/img/platt-plus.png" alt="Plus Members Image" />
    <h3 class="text-center remove-bottom-margin"> Get Started Today </h3>
    <h4 class="text-center plus-member-details"> Become a <span class="highlight-text"> Platt Plus </span> Member. </h4>
    <button class="learn-more-btn"> Learn More </button>
  </div>
</template>

<script>
  export default {
    name: 'content-plus-member'
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/colors.scss';

  .content-plus-member {
    text-align: center;
    padding: 30px 10px 40px;
  }

  .remove-bottom-margin {
    margin-bottom: 0;
  }

  .highlight-text {
    color: $content-panel-highlight-txt;
  }

  .plus-member-details {
    margin-top: 3px;
    margin-bottom: 15px;
  }

  .learn-more-btn {
    background-color: $light-grey;
    border-radius: 25px;
    padding: 12px 10px;
    border: none;
    outline: none;
    max-width: 200px;
    font-size: 14px;
    width: 100%;
    cursor: pointer;
  }

</style>