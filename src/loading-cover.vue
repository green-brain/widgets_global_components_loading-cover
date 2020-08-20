<template>
  <div class="loading" v-if="loading">
    <div class="spinner"></div>
  </div>
</template>

<script>
  export default {
    name: 'LoadingCover',

    props: ['loading'],
  }
</script>

<style lang="scss" scoped>
  $size: 100px;
  $desktopSize: 40px;

  .spinner {
    &:before {
      animation: spin 1s linear infinite, border-color-fade 1s linear infinite;
      content: '';
      display: inline-block;
      width: $size;
      height: $size;
      border-radius: 50%;
      border-style: solid;

      @media only screen and (min-width: 1024px) {
        width: $desktopSize;
        height: $desktopSize;
        border-width: 2px;
      }
    }
  }

  .loading {
    transition: opacity 1s linear;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1000;
    opacity: 1;

    .spinner {
      position: fixed;
      top: 20px;
      right: 18px;

      @media only screen and (min-width: 1024px) {
        right: 40px;
      }
    }
  }

</style>
