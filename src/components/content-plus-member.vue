<template>
  <div class="content-plus-member">
    <img src="../assets/img/platt-plus.png" alt="Plus Members Image" />
    <div class="plus-member-details-container">
      <h3 class="text-center remove-bottom-margin"> Get Started Today </h3>
      <h4 class="text-center plus-member-details"> Become a <span class="highlight-text"> Platt Plus </span> Member. </h4>
      <button class="btn-basic learn-more-btn"> Learn More </button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'content-plus-member'
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
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
    max-width: 200px;
    font-size: 14px;
  }

  @media screen and (min-width: $mobile-conatiner) {
    .content-plus-member {
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
      padding: 30px 30px 40px;
    }

    .plus-member-details-container {
      text-align: center;
      width: 50%;

      h3 {
        font-size: 20px;
      }

      h4 {
        font-size: 18px;
      }
  
      .learn-more-btn {
        font-size: 16px;
        max-width: 230px;
      }

    }
  }

</style>