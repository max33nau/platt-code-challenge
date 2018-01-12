<template>
  <div>
    <div class="search-box-container">
      <input name="searchDogs" class="search-base search-input" 
        type="text" 
        placeholder="What are you looking for?"
        v-model="breed"
        @keydown.enter="displayDogBreed" 
      />
      <div class="search-base search-icon-container"
        @click="displayDogBreed"
      > 
        <img 
          src="../assets/img/icons/black/ic_search.png" 
          alt=""
        />
      </div>
    </div>
    <v-modal v-if="showModal" @close="showModal = false">
      <img 
        slot="image"
        style="max-width: 100%;"
        :src="dogImageSrc"
      />
      <h3 slot="header">Dog Breed - {{breed}} </h3>
    </v-modal>
  </div>
</template>

<script>
  import VModal from './v-modal'

  import AutoComplete from 'js-autocomplete'
  import request from 'superagent'

  var data = {
    showModal: false,
    dogImageSrc: '',
    breed: '',
    dogBreeds: []
  }

  request
    .get('https://dog.ceo/api/breeds/list')
    .end((err, response) => {
      if (err) return
      var json = JSON.parse(response.text)
      data.dogBreeds = json.message
      /* eslint-disable no-new */
      new AutoComplete(
        {
          selector: 'input[name="searchDogs"]',
          minChars: 1,
          source: function (value, suggest) {
            var subDogBreedVal = value.toLowerCase()
            var matches = data.dogBreeds.filter((dog) => {
              var subDogText = dog.substring(0, value.length).toLowerCase()
              return subDogText === subDogBreedVal
            })
            suggest(matches)
          },
          onSelect: function (e, dogBreed, item) {
            data.breed = dogBreed
          }
        }
      )
    })

  export default {
    name: 'search-box',
    data: function () {
      return data
    },
    methods: {
      displayDogBreed: function () {
        var dogBreed = this.breed.toLowerCase()
        var matches = this.dogBreeds.filter((dog) => {
          return dogBreed === dog
        })
        var matchedDog
        matchedDog = matches[0]
        if (matchedDog) {
          request
            .get('https://dog.ceo/api/breed/' + matchedDog + '/images/random')
            .end((err, response) => {
              if (err) return
              var json = JSON.parse(response.text)
              data.dogImageSrc = decodeURIComponent(json.message)
              data.showModal = true
            })
        }
      }
    },
    components: {
      'v-modal': VModal
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
  @import '../assets/vendor/auto-complete.css';

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
      font-size: 16px;
      padding: $search-box-padding;
      width: 90%;
      border: none;
      outline: none;
      border-top-left-radius: $border-radius;
      border-bottom-left-radius: $border-radius;
      border-top-right-radius: 0;
      border-bottom-right-radius: 0;

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
      cursor: pointer;
      border-top-right-radius: $border-radius;
      border-bottom-right-radius: $border-radius;
      padding-right: $search-box-padding; 
      img {
        margin-top: $search-box-padding;
      }
    }

  }

  @media screen and (min-width: $mobile-conatiner) {
    .search-box-container {
      padding: 10px 3px 5px;
    }
  } 

</style>
