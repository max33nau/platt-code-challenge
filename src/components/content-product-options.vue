<template>
  <div class="content-product-options">
    <div class="product-option"
      v-for="option in productOptions"
      :key="option.id"
    >
      <button class="product-option-button">
        <img 
          :src="option.icon"
          alt="Click Me" 
        />
      </button>
      <div class="product-text"> {{option.text}} </div>
    </div>
  </div>
</template>

<script>
  import categoryIcon from '../assets/img/icons/green/ic_line_style.png'
  import searchIcon from '../assets/img/icons/green/ic_search.png'
  import scanIcon from '../assets/img/icons/green/ic_scanner.png'

  export default {
    name: 'content-product-options',
    data: function () {
      return {
        productOptions: [
          {
            id: 1,
            text: 'Categories',
            icon: categoryIcon
          },
          {
            id: 2,
            text: 'Search',
            icon: searchIcon
          },
          {
            id: 3,
            text: 'Scan',
            icon: scanIcon
          }
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
  @import '../assets/scss/colors.scss';

  .content-product-options {
    white-space: nowrap;
    margin: 0 auto;
    text-align: center;
    padding: 20px;
    display: flex;
    justify-content: space-between;
  }

  .product-option {
    display: inline-block;

    $icon-container-circle: 65px;
    $border-shadow: inset  0px -2px 0px rgba(0,0,0,0.4);
    .product-option-button {
      background-color: white;
      border-radius: 100%;
      width: $icon-container-circle;
      height: $icon-container-circle;
      margin: 0 auto;
      border: 1px solid #ccc;
      display: flex;
      justify-content: center;
      align-items: center;
      -webkit-box-shadow: $border-shadow;
      -moz-box-shadow: $border-shadow;
      box-shadow: $border-shadow;
      cursor: pointer;

      img {
        vertical-align: middle;
      }
    }

    .product-text {
      display: inline-block;
      margin-top: 7px;
      font-size: 14px;
    }
  }

</style>