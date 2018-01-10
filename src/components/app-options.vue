<template>
  <div class="options-container">
    <ul class="options-list">
      <li 
        v-for="option in options" 
        :key="option.id" 
        :class="option.itemClass ? option.itemClass : 'list-item'"
        @click="option.onClick"
      > 
        <div class="option-details-container">
          <div class="option-icon-container"> 
            <img class="option-icon"
              :src="option.icon"
              alt="" 
            />            
          </div>
          <span class="option-text">
            {{option.text}}
          </span>
        </div>
        <div class="arrow-container">
          <img class="arrow-icon"
            src="../assets/img/icons/black/ic_arrow_forward.png"
            alt="Click Here"
          />         
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  import categoryIcon from '../assets/img/icons/black/ic_categories.png'
  import catalogIcon from '../assets/img/icons/black/ic_playlist_add_check.png'
  import listIcon from '../assets/img/icons/black/ic_list.png'
  import helpIcon from '../assets/img/icons/green/ic_chat - active.png'
  import pimIcon from '../assets/img/icons/black/ic_check_circle.png'
  import personIcon from '../assets/img/icons/black/ic_person.png'
  import branchIcon from '../assets/img/icons/black/ic_place.png'

  export default {
    name: 'app-options',
    data: function () {
      return {
        options: [
          {
            id: 1,
            text: 'Shop all categories',
            icon: categoryIcon,
            onClick: () => alert('Shop all categories'),
            itemClass: 'all-categories-item'
          },
          {
            id: 2,
            text: 'My Catalog',
            icon: catalogIcon,
            onClick: () => alert('My Catalog')
          },
          {
            id: 3,
            text: 'My List',
            icon: listIcon,
            onClick: () => alert('My List')
          },
          {
            id: 4,
            text: 'Live Help',
            icon: helpIcon,
            onClick: () => alert('Live Help')
          },
          {
            id: 5,
            text: 'PIM',
            icon: pimIcon,
            onClick: () => alert('PIM')
          },
          {
            id: 6,
            text: 'Account',
            icon: personIcon,
            onClick: () => alert('Account')
          },
          {
            id: 7,
            text: 'Branch Locations',
            icon: branchIcon,
            onClick: () => alert('Branch Locations')
          }
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';

  .options-container {

    $padding-option-horizontal: 20px;
    $margin-option-horizontal: 10px;

    .option-details-container {
      max-width: 90%;
      width: 100%;
      display: inline-block;
    }

    .options-list {
      list-style-type: none;
      margin: 0;
      padding: 0 0 10px 0px;

      .list-item {
        white-space: nowrap;
        padding: 10px $padding-option-horizontal;
        font-size: 14px;
        border-top: 1px solid #ccc;
        margin: 0 $margin-option-horizontal;
        cursor: pointer;
      }

    }

    .all-categories-item {
      padding: 20px $padding-option-horizontal + $margin-option-horizontal;
      font-size: 16px;
      white-space: nowrap;
      cursor: pointer;

      .option-text {
        font-weight: bold;
      }
    }

    .option-text {
      vertical-align: middle;
      display: inline-block;
    }  

    .option-icon-container {
      width: 20px;
      display: inline-block;
      margin-right: 8px;
      text-align: center;

      .option-icon {
        vertical-align: middle;
        display: inline-block;
      }      
    }

    .arrow-container {
      max-width: 10%;
      width: 100%;
      text-align: right;
      display: inline-block;

      .arrow-icon {
        vertical-align: middle;
      }
    }
  }
</style>
