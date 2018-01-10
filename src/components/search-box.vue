<template>
  <div class="search-box-container">
    <input class="search-base search-input" 
      type="text" 
      placeholder="What are you looking for?" 
    />
    <div class="search-base search-icon-container"> 
      <img 
        src="../assets/img/icons/black/ic_search.png" 
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'search-box',
  data: function () {
    return {}
  }
}
</script>

<style lang="scss" scoped>

  .search-box-container {
    padding: 20px 12px;
    width: 100%;

    $border-radius: 4px;
    $search-box-padding: 15px;

    .search-base {
      background-color: #fff;
      display: inline-block;
      height: 45px;
    }

    .search-input {
      font-size: 14px;
      padding: $search-box-padding;
      width: 90%;
      border: none;
      outline: none;
      border-top-left-radius: $border-radius;
      border-bottom-left-radius: $border-radius;

      $place-holder-color: #a5a4ac;

      &::-webkit-input-placeholder {
        color: $place-holder-color;
      }

      &::-moz-placeholder { /* Firefox 19+ */
        color: $place-holder-color;
      }

      &:-ms-input-placeholder { /* IE 10+ */
        color: $place-holder-color;
      }
      
      &:-moz-placeholder { /* Firefox 18- */
        color: $place-holder-color;
      }     
    }


    
    .search-icon-container {
      width: 10%;
      float: right;
      text-align: right;
      border-top-right-radius: $border-radius;
      border-bottom-right-radius: $border-radius;
      padding-right: $search-box-padding; 
      img {
        margin-top: $search-box-padding;
      }
    }
  }

</style>
