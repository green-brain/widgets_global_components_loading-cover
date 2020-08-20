<script>
import Vue from 'vue';
import LoadingCover from '@/loading-cover.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    LoadingCover
  }
});
</script>

<template>
  <div id="app">
    <loading-cover />
  </div>
</template>
