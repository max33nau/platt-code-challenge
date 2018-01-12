
<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-header">
            <slot name="header">
              default header
            </slot>
          </div>
          <div class="modal-image-container">
            <slot name="image">
              Image for modal goes here
            </slot>
          </div>
          <div class="modal-footer">
            <button class="btn-basic modal-default-button" @click="$emit('close')">
              OK
            </button>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
  // this modal component was retrieved from https://vuejs.org/v2/examples/modal.html

  export default {
    name: 'v-modal'
  }
</script>

<style lang="scss" scoped>
  @import '../assets/scss/layout.scss';
  @import '../assets/vendor/auto-complete.css';

  .modal-mask {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, .5);
    display: table;
    transition: opacity .3s ease;
  }

  .modal-wrapper {
    display: table-cell;
    vertical-align: middle;
  }

  .modal-container {
    width: 300px;
    margin: 0px auto;
    padding: 0;
    background-color: #fff;
    border-radius: 2px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, .33);
    transition: all .3s ease;

  }

  .modal-image-container {
    text-align: center;
    padding: 0 10px;
  }

  .modal-header {
    text-align: center;
    padding: 5px;
  }

  .modal-footer {
    text-align: center;
    padding: 20px;
  }

  .modal-default-button {
    max-width: 200px;
  }

  .modal-enter {
    opacity: 0;
  }

  .modal-leave-active {
    opacity: 0;
  }

  .modal-enter .modal-container,
  .modal-leave-active .modal-container {
    -webkit-transform: scale(1.1);
    transform: scale(1.1);
  }

</style>
