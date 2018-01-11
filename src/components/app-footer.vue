<template>
  <footer class="footer">
    <div class="footer-content">
      <h4 class="header"> Support Center </h4>
      <h4 class="header header-with-sub"> 800-25-Platt </h4>
      <h5 class="sub-header"> 800-257-5288 </h5>
      <h4 class="header header-with-sub footer-dark-txt"> 4 a.m. - 12 a.m. (pst) </h4>
      <h4 class="header footer-dark-txt"> 7 Days a week </h4>
      <button class="btn-basic live-help-btn">  
        <img src="../assets/img/icons/black/ic_comment.png" />
        <span> Live Help </span>
      </button>     
    </div>

    <ul class="footer-options">
      <li> Contact Us </li>
      <li> What's New </li>
      <li> FAQ's </li>
    </ul>
  </footer>
  
</template>

<script>
  export default {
    name: 'app-footer'
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
  @import '../assets/scss/colors.scss';

  .footer {
    background-color: $dark-grey;
    color: $footer-txt;
    padding-bottom: 30px;

    .footer-content {
      padding: 30px 15px;
      text-align: center;
    }


    .footer-dark-txt {
      color: $footer-darg-txt;
    }

    .header {
      text-align: center;
      margin-top: 0;
      margin-bottom: 10px;
      font-size: 18px;
    }

    .header-with-sub {
      margin-bottom: 0px;
    }

    .sub-header {
      text-align: center;
      margin-top: 0;
      margin-bottom: 10px;
      font-size: 14px;
      font-weight: normal;
    }

    .live-help-btn {
      background-color: $light-grey;
      max-width: 220px;
      margin: 20px auto;
      padding: 11px;

      img {
        vertical-align: text-top;
        margin-right: 5px;
      }

      span {
        display: inline-block;
        vertical-align: middle;
      }
    }

    .footer-options {
      padding: 0;
      display: flex;
      list-style: none;
      justify-content: space-around;
      font-size: 14px;
      margin-bottom: 0;
      margin-top: 40px;

      li:hover {
        opacity: .5;
      }
    }

    @media screen and (min-width: $mobile-conatiner) {
      .header {
        font-size: 22px;
      }

      .sub-header {
        font-size: 16px;
      }

      .live-help-btn {
        max-width: 240px;
        margin: 20px auto;
        padding: 14px;
        font-size: 16px;
      }

      .footer-options {
        font-size: 16px;
        margin-top: 10px;
      }
    }

  }


</style>
