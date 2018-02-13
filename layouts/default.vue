
<template>
  <div id="app" class="container">
    <menupane/>
    <nuxt class="main-content" />
  </div>
</template>

<script>
  import menupane from '@/components/menupane';

  export default {
    name: 'app',
    components: {
      menupane
    },
    mounted() {},
    data() {
      return {}
    }
  }
</script>

<style lang="scss">
  @import './assets/css/main.scss';
</style>
