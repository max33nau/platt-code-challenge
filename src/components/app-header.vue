<template>
  <div class="header">

    <img class="logo" 
      src="../assets/img/logo.png" 
      alt="Platt logo"
    />
    <ul class="nav-list">
      <li> 
        <img src="../assets/img/icons/white/ic_search.png" /> 
      </li>
      <li> 
        <img src="../assets/img/icons/white/ic_shopping_cart.png" /> 
      </li>
      <li> 
        <img src="../assets/img/icons/white/ic_person.png" /> 
        <span v-if="personNotify" class="notification"> </span>
      </li>
      <li> 
        <img src="../assets/img/icons/white/ic_menu.png" /> 
      </li>
    </ul>
    <search-box> </search-box>
  </div>
</template>

<script>
  import SearchBox from './search-box.vue'

  export default {
    name: 'app-header',
    data: function () {
      return {
        personNotify: true
      }
    },
    components: {
      'search-box': SearchBox
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
  @import '../assets/scss/colors.scss';

  .header {
    background-color: $dark-green;
    width: 100%;
    padding: 10px;
  }

  .nav-list {
    float: right;
    list-style: none;
    margin: 0;
    padding: 0;
    
    li {
      display: inline-block;
      margin: 0 8px;
      vertical-align: middle;
      position: relative;
      cursor: pointer;
    }

    $box-shadow: 0px 1px 2px 1px rgba(0,0,0,.35);

    .notification {
      position: absolute;
      width: 5px;
      height: 5px;
      background-color: #ffbf30;
      border-radius: 100%;
      top: -3px;
      right: -7px;
      -webkit-box-shadow: $box-shadow;
      -moz-box-shadow: $box-shadow;
      box-shadow: $box-shadow;
    }
  }

</style>
